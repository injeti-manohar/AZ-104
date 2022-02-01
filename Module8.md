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




