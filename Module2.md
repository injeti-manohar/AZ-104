**Why compliance & governance??**
It help maintain the balance between what is needed versus what is delivered

[According to lucidchart](https://www.lucidchart.com/blog/cloud-governance-framework) helps maintain cost savings and meet company's need with cloud in a structured way.

[MS Docs](https://docs.microsoft.com/en-us/learn/modules/cloud-adoption-framework-govern/1-introduction) says it's a important concern for company's migrating to cloud. 

![](https://docs.microsoft.com/en-us/learn/modules/cloud-adoption-framework-govern/media/methodology.png)

## Region

zone-redundant service	An Azure service that supports availability zones, and that enables resources to be replicated or distributed across zones automatically.

![](https://docs.microsoft.com/en-us/azure/availability-zones/media/availability-zones.png)

**Availability zones**
Each zone is composed of one or more datacenters equipped with independent power, cooling, and networking infrastructure.
You can design resilient solutions by using Azure services that use availability zones. Co-locate your compute, storage, networking, and data resources across an availability zone, and replicate this arrangement in other availability zones

**Region Pair**

![](https://docs.microsoft.com/en-us/azure/availability-zones/media/availability-zones-region-geography.png)

## Subscription
> Decides how resource usage is reported, billed, and paid for.

- Each subscription offers Different Billing Period, Resources and Reporting features.

 <br>    *Like in Azure for Student Subscription, You Can't Use AZURE CDN ; While in PAY-AS-GO You can !!*
     Also You can't setup Billig alerts in AZ for Student. You can't see the credits remaining from the portal.
     Another example -- FOR Enterprise Agreement You PAY ANNUALLY. while In PAY-AS-GO MONTHLLY

- Billing boundary : When Billed, How much can you spend (Free trial Has $200 Credits, PAY-AS-GO -> No limit `unless you create a limit`)
- Access control boundary : Give, Remove permissions on Subscription level.
![How Azure AD Is Linked to subscription](https://github.com/Ananyojha/spare-images/blob/main/AD%20vs%20AAD-Page-1.jpg?raw=true)

- why organization need multiple subscription ?
- [x] Organizations often use multiple Azure subscriptions to avoid per-subscription resource limits and to better manage and govern their Azure resources
<br> Like for Production Env. You Have Enterprise Agreement while for training Purposes, You have Free Trial 

## types of Azure Subscription

`*Enterprise agreements*`
Any Enterprise Agreement customer can add Azure to their agreement by making an upfront monetary commitment to Azure. That commitment is consumed throughout the year by using any combination of the wide variety of cloud services Azure offers. An Enterprise Agreement provides flexibility to buy cloud services and software licenses under one agreement, with discounts for new licenses and Software Assurance. It's targeted at enterprise-scale organizations. Enterprise agreements have a 99.95% monthly SLA.

<br>`*Reseller*`
Buy Azure through the Open Licensing program, which provides a simple, flexible way to purchase cloud services from your Microsoft reseller. If you already purchased an Azure in Open license key, activate a new subscription or add more credits now.

`*Partners*`
Find a Microsoft partner who can design and implement your Azure cloud solution. These partners have the business and technology expertise to recommend solutions that meet the unique needs of your business. Just Like a Cyber Cafe, 

`PAYG`
A Pay-As-You-Go (PAYG) subscription charges you monthly for the services you used in that billing period. This subscription type is appropriate for a wide range of users, from individuals to small businesses, and many large organizations as well.

`Personal free account`
With a free trial account, you can get started using Azure right away and you won’t be charged until you choose to upgrade to PAYG. Ideal for Learning and exploring Azure.

## Tags 
> helps Identify and arrange Resources

- Each resource or resource group can have a maximum of 50 tag name/value pairs.
- Tags applied to the resource group are not inherited by the resources in that resource group.

### Cost Management and billing
> Monitor, control and optimise your cloud expenditure

- `cost analysis` : Reports in Cost Management show the usage-based costs consumed by Azure services and third-party Marketplace offerings

- ` Alerts` -- You can configure alerts based on your actual cost or forecasted cost to ensure that your spend is within your organizational spend limit  
<br>
- [x] only notification send and resources are not terminated

- `Recommendations`: It shows how you can optimize and improve efficiency by identifying idle and underutilized resources. Or, they can show less expensive resource options. When you act on the recommendations, you change the way you use your resources to save money. To act, you first view cost optimization recommendations to view potential usage inefficiencies. Next, you act on a recommendation to modify your Azure resource use to a more cost-effective option. Then you verify the action to make sure that the change you make is successful.

- `Monitor` -- understand where costs originated within your organization. It's also useful to know how much money your services cost
-  And you can set a daily scheduled export in CSV format and store the data files in Azure storage. Then, you can access the data from your external system.
<br> - manage both AWS (small charge) and Azure (free)
     - various connectors also available like power BI
     
     --------------
     
> Your company is subject to many regulations and compliance rules. They want to ensure each department implements and deploys resources correctly.

## management group
-  your organization has several subscriptions, you may need a way to efficiently manage access, policies, and compliance for those subscriptions. Azure management groups provide a level of scope above subscriptions `All subscriptions within a management group automatically inherit the conditions applied to the management group`
-  Mirror your organisation’s structure so that 
<br>  - Organizational alignment for your Azure subscriptions through custom hierarchies and grouping.
- Targeting of policies and spend budgets across subscriptions and inheritance down the hierarchies.
- Compliance and cost reporting by organization (business/teams).


### Azure Policy 
> enforce rules to your resources
> 
- help ensure cloud compliance, avoid misconfigurations and practice consistent resource governance
- Comprehensive compliance view of all your resources
- Real-time policy enforcement and evaluation
- Define a scope ; Yes, you may exclude a resource, resource group, subscription or management group from your policy assignment.
**An Azure Policy as Code workflow makes it possible to manage your policy definitions and assignments as code, control the lifecycle of updating those definitions, and automate the validating of compliance results**

`Use cases`
- Specify the resource types that your organization can deploy.
- Specify a set of virtual machine SKUs that your organization can deploy.
- Restrict the locations your organization can specify when deploying resources.
- Enforce a required tag and its value.
- Audit if Azure Backup service is enabled for all Virtual machines.

----------------

> Securing your Azure resources, such as virtual machines, websites, networks, and storage, is a critical function for any organization using the cloud. 
`Basics Principle Of Security : Trust No One ! --> No Extra Permissions to anyone.`

## RBAC 

### concepts 
`Security principal`. Object that represents something that is requesting access to resources. Examples: user, group, service principal, managed identity

`Role definition.` Collection of permissions that lists the operations that can be performed. Examples: Reader, Contributor, Owner, User Access Administrator

`Scope`. Boundary for the level of access that is requested. Examples: management group, subscription, resource group, resource

`Assignment`. Attaching a role definition to a security principal at a particular scope. Users can grant access described in a role definition by creating an assignment. Deny assignments are currently read-only and can only be set by Azure.

`Owner`. Has full access to all resources including the right to delegate access to others. The Service Administrator and Co-Administrators are assigned the Owner role at the subscription scope.
`Contributor`. Can create and manage all types of Azure resources but can’t grant access to others.
`Reader`. Can view existing Azure resources.
`User Access Administrator`. Lets you manage user access to Azure resources, rather than to managing resources.

There are other built-in roles. 

For example, the `Virtual Machine Contributor` role allows a user to create and manage virtual machines.
When the built-in roles don't meet the specific needs of your organization, you can create your `own custom roles`.
Roles can grant access to `data within an object`. For example, if a user has read data access to a storage account, then they can read the blobs or messages in the storage account.
