![](https://docs.microsoft.com/en-us/learn/modules/control-network-traffic-flow-with-routes/media/2-system-routes-subnets-internet.svg)

Within Azure, there are additional system routes. Azure will create these routes if the following capabilities are enabled:

- Virtual network peering
- Service chaining
- Virtual network gateway
- Virtual network service endpoint

- `Virtual network peering` and `service chaining` let virtual networks within Azure be connected to one another. Regionally or Globally

- Use a `virtual network gateway` to send encrypted traffic between Azure and on-premises over the internet and to send encrypted traffic between Azure networks. A virtual network gateway contains routing tables and gateway services.

- `Virtual network endpoints` provides a direct connection to your Azure resources. This connection restricts the flow of traffic: your Azure virtual machines can access your storage account directly from the private address space and deny access from a public virtual machine. As you enable service endpoints, Azure creates routes in the route table to direct this traffic.
- The rule addition provides improved security by fully removing public internet access to resources and allowing traffic only from your virtual network.

**Why Custom Routes (User Defined Routes)**

NVA helps network virtual appliance (NVA) to help secure and monitor traffic 
- You can use an NVA to filter traffic inbound to a virtual network, to block malicious requests, and to block requests made from unexpected resources.
so for example, you might want to route traffic through an NVA or through a firewall from partners and others. This control is possible with custom routes.

*Two methods for this*
1. create a `user-defined route` :-
- [x] traffic flow via a firewall to your subnet 
For example, you might have a network with two subnets and want to add a virtual machine in the perimeter network to be used as a firewall. You create a user-defined route so that traffic passes through the firewall and doesn't go directly between the subnets.
Specify next hop type - 
- NVA 
- vnet gateway, internet or
- None 

![](https://docs.microsoft.com/en-us/learn/modules/control-network-traffic-flow-with-routes/media/4-nva.svg)

or use 
2. `Border Gateway Protocol (BGP)` to exchange routes between Azure and on-premises networks
As we know BGP is a standard routing protocol used by internet and other autonomous systems.

### Service Endpoints

The rule addition provides improved security by fully removing public internet access to resources and allowing traffic only from your virtual network.

• **Improved security for your Azure service resources** - use private ip of your vm and attach a service endpoint policy to provide 

• **Optimal routing for Azure service traffic from your virtual network** - 

• **less management** - There are no Network Address Translation (NAT) or gateway devices required to set up the service endpoints. You can configure service endpoints through a simple click on a subnet. There's no additional overhead to maintaining the endpoints 

**There's no additional charge for using service endpoints. No limits for no. Of endpoints**

### NVA FOR HIGH AVAILABILITY

NVA starts acting as a router. If traffic is routed through an NVA, the NVA becomes a critical piece of your infrastructure. Any NVA failures will directly affect the ability of your services to communicate. It's important to include a highly available architecture in your NVA deployment.

So, A network gateway in your on-premises network can exchange routes with a virtual network gateway in Azure by using BGP. 

### Azure Load Balancer
> Many apps need to be resilient to failure and scale easily when demand increases. You can address those needs by using Azure Load Balancer.

Backend pool With Load Balancer, you can use availability sets (SLA OF 99.95)and availability zones (99.99) to ensure that virtual machines are always available

### Layer 7 LB
 - Layer 7 load balancers base their routing decisions on various characteristics of the HTTP header and on the actual contents of the message, such as the URL, the type of data (text, video, graphics), or information in a cookie. It can determine what type of data (video, text, and so on) a client is requesting, you don’t have to duplicate the same data on all of the load-balanced servers.
- powerful enough that the savings in computational cost from Layer 4 load balancing are not large enough to outweigh the benefits of greater flexibility and efficiency from Layer 7 load balancing. 
*Source* : [Nginx](https://www.nginx.com/resources/glossary/layer-4-load-balancing/?__cf_chl_captcha_tk__=J.wHM4ZZIPckeYhRZqZkDzK7pokpeDAq4xyOiYkew5A-1643538508-0-gaNycGzNCL0)

### Azure application Load Balancer
by default uses round Robin but you can also specify session stickiness

- Additional benefits
- Support for the HTTP, HTTPS, HTTP/2 and WebSocket protocols.
- A web application firewall to protect against web application vulnerabilities.
- End-to-end request encryption.
- Autoscaling, to dynamically adjust capacity as your web traffic load change

`URL path based routing` -- docs.microsoft.com/learn or docs.microsoft.com/azure

`Multi site routing` -- register multiple DNS names (CNAMEs) for the IP address of the Application Gateway, specifying the name of each site. 
