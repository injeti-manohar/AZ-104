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


### management group
- Mirror your organisation’s structure

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

### Azure Policy 
- help ensure cloud compliance, avoid misconfigurations and practice consistent resource governance
- Comprehensive compliance view of all your resources
- Real-time policy enforcement and evaluation
- Define a scope ; Yes, you may exclude a resource, resource group, subscription or management group from your policy assignment.
**An Azure Policy as Code workflow makes it possible to manage your policy definitions and assignments as code, control the lifecycle of updating those definitions, and automate the validating of compliance results**
