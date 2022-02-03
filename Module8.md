# Azure VM
Your organization Not wanting to be constrained by the limitations of on-premises infrastructure, Pearson VUE created a five-year plan to migrate legacy on-premises applications and data to the cloud.
As an Admin your tasks will include correctly sizing the machines, selecting storage, and configuring networking for 

#### module overview
> As you wish

#### IaaS -- Shared responsibility 
- Azure Virtual Machines is one of several types of on-demand, scalable computing resources that Azure 
- Virtual machines are part of the Infrastructure as a Service (IaaS) offering. IaaS is an instant computing infrastructure, provisioned and managed over the Internet. Quickly scale up and down with demand and pay only for what you use.
- Gives more freedom over operating system, storage, and networking capabilities and can run a wide range of applications.
So, works like your Datacentre on cloud.

#### IaaS business scenarios
- Teams can quickly set up and dismantle test and development environments
- High-performance computing (HPC) include earthquake and protein folding simulations, climate and weather predictions, financial modeling, and evaluating product designs.

#### Shared Responsibility

### virtual Machine planning
 > Gi to portal check slides. Create a WINDOW IN PORTAL & linux (IN CLOUD SHELL) VM
[USE MS DOCS FOR EXPLAINING](https://docs.microsoft.com/en-us/learn/modules/configure-virtual-machines/3-plan) 

### VM CONNECTION SLIDE NO 11 
> CONNECT TO WINDOWS USING RDP & LINUX USING CLOUD SHELL

## lesson 2 : VM AVAILABLITY

#### maintance vs downtime
As an Azure administrator you must be prepared for planned and unplanned failures

##### unplanned hardware failures - 
When azure finds any physical infra of your VM is falling, there's unplanned hardware maintenance event. Azure uses Live Migration technology to migrate the Virtual Machines from the failing hardware to a healthy physical machine.
- this only pauses the Virtual Machine for a short time, 

#### unexpected downtimes
when the hardware or the physical infrastructure for the virtual machine fails unexpectedly. I.e any rack level failure occurs
- When detected, the Azure platform automatically migrates (heals) your virtual machine to a healthy physical machine in the same datacenter. During the healing procedure, virtual machines experience downtime (reboot) and in some cases loss of the temporary drive.

#### planned updates
Microsoft have their internal update calendar. 
- So customers get best experience
- Most of these updates are performed without any impact upon your Virtual Machines or Cloud Services.

> To prevent from data centre level failures we have -- 

### Availability Sets 
- prevents your application from data centre level failures
- Azure ensures that the VMs you place within an Availability Set run across multiple physical servers, compute racks, storage units, and network switches. If a hardware or Azure software failure occurs, only a subset of your VMs are impacted. Your application stays up and continues to be available to your customers.

> So how you ensure uptime

- by deploying more than 1 VM across Availability SETS 
- VM CAN ONLY BE ADDED IN A AVAILABLITY SET AT TIME OF CREATION.... NOT AFTER THAT

### Update and fault domains

Each virtual machine in an availability set is placed in one update domain and one fault domain

- `UPDATE DOMAIN` -- a set of virtual machines and associated physical hardware that can be updated and rebooted at the same time
- `FAULT DOMAIN` -- A fault domain defines a group of virtual machines that share a common set of hardware, switches, that share a single point of failure.

![](https://docs.microsoft.com/en-us/learn/wwl-azure/configure-virtual-machine-availability/media/update-fault-domains-c1ceee00.png)

⏫ Here is shown how a Availability set works, 2 VM in Availability set are in 2 diff racks hence diff `fault domain` 

> Please note that Placing your virtual machines into an availability set does not protect your application from operating system or application-specific failures. For that, you need to review other disaster recovery and backup techniques

💪 WHAT IF ENTIRE DATA CENTRE GOES DOWN ?

### Availability Zones
Usually within a region, azure has 3 or more Datacentres i.e 3 or more Availability Zones
- Each zone is made up of one or more datacenters equipped with independent power, cooling, and networking

Azure services that support Availability Zones fall into two categories:

- `Zonal services`. Pins the resource to a specific zone (for example, virtual machines, managed disks, Standard IP addresses).

- `Zone-redundant` services. Platform replicates automatically across zones (for example, zone-redundant storage, SQL Database).

 > To make sure your application is always available, 

### vertical and horizontal scaling

#### vertical scaling -- 
means increasing or decreasing virtual machine sizes 

- Vertical scaling makes the virtual machines more (scale up) or less (scale down) powerful. Vertical scaling can be useful when:

`Example` -- 
 - A service built on virtual machines is under-utilized (for example at weekends). Reducing the virtual machine size can reduce monthly costs.
- Increasing virtual machine size to cope with larger demand without creating additional virtual machines

`but resizing makes vm to restart`

#### Horizontal Scaling
Here you add similar machines or remove them referred to as scale out and scale in .

> If you want you can also configure auto scaling of vm using

### VM SCALE SETS 
- deploy and manage a set of VMs of same size and configuration.
- As demand goes up more virtual machine instances can be added. As demand goes down virtual machines instances can be removed. The process can be manual or automated or a combination of both.
- can be attached to azure load balancer or Application gateway as backend 

### auto scaling
Autoscale minimizes the number of unnecessary VM instances that run your application when demand is low, while customers continue to receive an acceptable level of performance as demand grows and additional VM instances are automatically added.

