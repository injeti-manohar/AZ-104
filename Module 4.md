## scenario
> Your company is migrating to Azure Your company requires an Azure IP addressing schema. The schema should provide flexibility, room for growth, and integration with on-premises networks. The schema should also minimize public exposure of systems, and give the organization flexibility in its network design. If not properly designed, systems might not be able to communicate, and additional work will be required to remediate.

NIC allows both wired and wireless communications. NIC allows communications between computers connected via local area network (LAN) as well as communications over large-scale network through Internet Protocol (IP).

While physical networking connects computers through cabling and other hardware, virtual networking extends these capabilities by using software management to connect computers and servers over the Internet
network administrators new and more efficient options, like the ability to easily modify the network as needs change, without having to switch out or buy more hardware. [Learn More from VMware](https://www.vmware.com/topics/glossary/content/virtual-networking.html#:~:text=Virtual%20networking%20is%20the%20foundation,secure%2C%20and%20modify%20cloud%20resources.)

##### Subnets 
- Security
- Traffic Reduction 
- Easy Administration 

[Learn more from CBT Nuggets](https://www.networkcomputing.com/data-centers/5-subnetting-benefits)

### vnet 

- `logical isolation of azure cloud` (define your own address range in CIDR)
- `Easy configuration and full control` (You also have control of DNS server settings for VNets, and segmentation of the VNet into subnets.)
-  `connect to other networks` (site-to-site for connecting on prem env or other networks... Hence enable communication between them)
- `implement hybrid scenario` (You can securely connect cloud-based applications to any type of on-premises system such as mainframes and Unix systems.)

### Subnets
- Each subnet contains a range of IP addresses that fall within the virtual network address space. 
- plan the address space for subnet as azure reserves 5 Addresses from your subnet
- helps implement specific networking rules.. like make VM inaccessible from internet via NSG
- [NVA](https://aviatrix.com/learn-center/cloud-security/azure-network-virtual-appliance/#:~:text=Azure%20network%20virtual%20appliance%20is,(DMZ)%20in%20the%20cloud.)


- [IP Address for Azure Deployment -- MS Learn](https://docs.microsoft.com/en-us/learn/modules/design-ip-addressing-for-azure/#:~:text=A%20good%20Azure%20IP%20addressing,organization%20flexibility%20in%20its%20network.)

- [Design Vnet for Azure](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/plan-for-ip-addressing) 

### Public IP Address Azure
- You can assign IP addresses to Azure resources to communicate with other Azure resources, your on-premises network, and the Internet 
-  You cannot change the SKU after the public IP address is created

**Types of IP addresses** 
- `Private IP addresses`: Used for communication within an Azure virtual network (VNet), and your on-premises network, when you use a VPN gateway or ExpressRoute circuit to extend your network to Azure.
- `Public IP addresses`: Used for communication with the Internet, including Azure public-facing services.

> whenever you stop and start the VM IP address associated with that Virtual Machine changes this is known as `dynamic IP addresses`

You can also associate a static IP address for following use cases:

- DNS name resolution, where a change in the IP address would require updating host records.
- IP address-based security models that require apps or services to have a static IP address.
- TSL/SSL certificates linked to an IP address.
- Firewall rules that allow or deny traffic using IP address ranges.
- Role-based VMs such as Domain Controllers and DNS servers

## Azure Firewalls
> Your company is spread across multiple Azure regions. The networking infrastructure includes multiple virtual networks and connections to an on-premises network. The IT staff is concerned about malicious actors trying to infiltrate the network.

Azure Firewall is a `PaaS service` ---> managed, cloud-based network security service

`NSG VS AZURE FIREWALL`

| NSG | AZ FIREWALL |
|------|-------|
| Stateless | stateful | 
| `Layer 4 (network)` i.e only concerned with source and destination ports and protocols | `(layer 7 + layer 4)` source protocol and the packets | 
| Can be attached to subnet or NIC card | |


## Azure DNS
Azure DNS enables you to host your DNS records for your domains on Azure infrastructure
> Whenever you create a new user in Azure active directory the user requires your domain name to sign into the portal. 

### Initial domain
When you create an Azure subscription, an Azure AD domain is automatically created. This instance of the domain has an initial domain name in the form `domainname.onmicrosoft.com` like `ananayojha@gmail.com.onmicrosoft.com`

### custom domain
If You own any domain name you can add that domain to add your active directory A custom domain name which simplifies the user sign-on experience. Like

## DNS ZONE 
A DNS zone hosts the DNS records for a domain. So, to start hosting your domain in Azure DNS, you need to create a DNS zone for that domain name. Each DNS record for your domain is then created inside this DNS zone.

- You do not have to own a domain name to create a DNS zone with that domain name in Azure DNS. However, you do need to own the domain to configure the domain
- Root/Parent domain is registered at the registrar and pointed to Azure NS.
- Child domains are registered in AzureDNS directly

