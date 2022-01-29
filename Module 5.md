- The traffic between virtual machines in peered virtual networks uses the Microsoft backbone infrastructure. Like traffic between virtual machines in the same network, traffic is routed through Microsoft's private network only

- The ability to transfer data between virtual networks across Azure subscriptions, Azure Active Directory tenants, deployment models, and Azure regions
- No downtime to resources in either virtual network when creating the peering, or after the peering is created
- For peered virtual networks, resources in either virtual network can directly connect with resources in the peered virtual network.

- The network latency between virtual machines in peered virtual networks in the same region is the same as the latency within a single virtual network
Apply NSG at one vnet ---> vnet (no NSG here rule same applies)


- Service chaining enables you to direct traffic from one virtual network to a virtual appliance or gateway in a peered network through user-defined routes

- peered virtual network, can have its own gateway. A virtual network can use its gateway to connect to an on-premises network

VPN GATEWAY-Azure VPN Gateway connects your on-premises networks to Azure through Site-to-Site VPNs in a similar way that you set up and connect to a remote branch office. The connectivity is secure and uses the industry-standard protocols Internet Protocol Security (IPsec) and Internet Key Exchange (IKE).
