`VpN Peering`
- The traffic between virtual machines in peered virtual networks uses the Microsoft backbone infrastructure. Like traffic between virtual machines in the same network, traffic is routed through Microsoft's private network only

- The ability to transfer data between virtual networks across Azure subscriptions, Azure Active Directory tenants, deployment models, and Azure regions
- No downtime to resources in either virtual network when creating the peering, or after the peering is created
- For peered virtual networks, resources in either virtual network can directly connect with resources in the peered virtual network.

- The network latency between virtual machines in peered virtual networks in the same region is the same as the latency within a single virtual network
Apply NSG at one vnet ---> vnet (no NSG here rule same applies)


- Service chaining enables you to direct traffic from one virtual network to a virtual appliance or gateway in a peered network through user-defined routes

- peered virtual network, can have its own gateway. A virtual network can use its gateway to connect to an on-premises network

`VPN GATEWAY`-Azure VPN Gateway connects your on-premises networks to Azure through Site-to-Site VPNs in a similar way that you set up and connect to a remote branch office. The connectivity is secure and uses the industry-standard protocols Internet Protocol Security (IPsec) and Internet Key Exchange (IKE).

`ExpressRoute` - Use ExpressRoute to set up a fast, private connection to Microsoft cloud services from your on-premises infrastructure or co-location facility. You can create a connection between your on-premises network and the Microsoft cloud in three different ways, CloudExchange Co-location, Point-to-point Ethernet Connection, and Any-to-any (IPVPN) Connection. Connectivity providers can offer one or more connectivity models. You can work with your connectivity provider to pick the model that works best for you.

`VIrtual WAN` - Create a virtual WAN to get started. Next, create sites in your virtual WAN and connect them to virtual hubs in your preferred Azure regions. Within your virtual WAN, you can also connect hubs to your existing virtual networks.

- Basic virtual WAN supports Site-to-Site VPN connectivity, branch-to-branch and branch-to-VNet connectivity in a single hub.
Standard Virtual WAN supports any-to-any connectivity (Site-to-Site VPN, VNET, ExpressRoute, Point-to-site end points) in a single hub as well as across hubs.
-A virtual hub is a Microsoft-managed virtual network. The hub contains various service endpoints to enable connectivity from your on-premises network (vpnsite). 

### NVA FOR HIGH AVAILABILITY

NVA starts acting as a router. If traffic is routed through an NVA, the NVA becomes a critical piece of your infrastructure. Any NVA failures will directly affect the ability of your services to communicate. It's important to include a highly available architecture in your NVA deployment.

So, A network gateway in your on-premises network can exchange routes with a virtual network gateway in Azure by using BGP.
