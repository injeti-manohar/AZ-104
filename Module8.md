# Azure VM
deployment tasks will include correctly sizing the machines, selecting storage, and configuring networking

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

- by deploying more than 1 VM across Availability Zones 
- VM CAN ONLY BE ADDED IN A AVAILABLITY ZONE AT TIME OF CREATION.... NOT AFTER THAT
