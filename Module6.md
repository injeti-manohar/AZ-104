![](https://docs.microsoft.com/en-us/learn/modules/control-network-traffic-flow-with-routes/media/2-system-routes-subnets-internet.svg)

Within Azure, there are additional system routes. Azure will create these routes if the following capabilities are enabled:

- Virtual network peering
- Service chaining
- Virtual network gateway
- Virtual network service endpoint

- `Virtual network peering` and `service chaining` let virtual networks within Azure be connected to one another. Regionally or Globally

- Use a `virtual network gateway` to send encrypted traffic between Azure and on-premises over the internet and to send encrypted traffic between Azure networks. A virtual network gateway contains routing tables and gateway services.

- `Virtual network endpoints` provides a direct connection to your Azure resources. This connection restricts the flow of traffic: your Azure virtual machines can access your storage account directly from the private address space and deny access from a public virtual machine. As you enable service endpoints, Azure creates routes in the route table to direct this traffic.
