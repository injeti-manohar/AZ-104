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
-  You cannot change the SKU after the public IP address is created
