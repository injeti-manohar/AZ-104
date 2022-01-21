### Subscription
> Decides how resource usage is reported, billed, and paid for.

- Each subscription offers Different Billing Period, Resources and Reporting features.

     *Like in Azure for Student Subscription, You Can't Use AZURE CDN ; While in PAY-AS-GO You can !!*
     Also You can't setup Billig alerts in AZ for Student. You can't see the credits remaining from the portal.
     Another example -- FOR Enterprise Agreement You PAY ANNUALLY. while In PAY-AS-GO MONTHLLY

- Billing boundary : When Billed, How much can you spend (Free trial Has $200 Credits, PAY-AS-GO -> No limit `unless you create a limit`)
- Access control boundary : Give, Remove permissions on Subscription level.
![How Azure AD Is Linked to subscription](https://github.com/Ananyojha/spare-images/blob/main/AD%20vs%20AAD-Page-1.jpg?raw=true)

- why organization need multiple subscription ?
- [x] Organizations often use multiple Azure subscriptions to avoid per-subscription resource limits and to better manage and govern their Azure resources


### management group
- Mirror your organisation’s structure

### Cost Management and billing
- Alerts -- You can configure alerts based on your actual cost or forecasted cost to ensure that your spend is within your organizational spend limit
     
 - [x] only notification send and resources are not terminated
- Monitor -- understand where costs originated within your organization. It's also useful to know how much money your services cost
- manage both AWS (small charge) and Azure (free)
- various connectors also available like power BI

### Azure Policy 
- help ensure cloud compliance, avoid misconfigurations and practice consistent resource governance
- Comprehensive compliance view of all your resources
- Real-time policy enforcement and evaluation
- Define a scope ; Yes, you may exclude a resource, resource group, subscription or management group from your policy assignment.
**An Azure Policy as Code workflow makes it possible to manage your policy definitions and assignments as code, control the lifecycle of updating those definitions, and automate the validating of compliance results**
