![](https://docs.microsoft.com/en-us/learn/modules/control-network-traffic-flow-with-routes/media/2-system-routes-subnets-internet.svg)

Within Azure, there are additional system routes. Azure will create these routes if the following capabilities are enabled:

- Virtual network peering
- Service chaining
- Virtual network gateway
- Virtual network service endpoint

- Virtual network peering and service chaining let virtual networks within Azure be connected to one another. Regionally or Globally

- Use a virtual network gateway to send encrypted traffic between Azure and on-premises over the internet and to send encrypted traffic between Azure networks. A virtual network gateway contains routing tables and gateway services.
