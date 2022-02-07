# Monitoring
Suppose that you work for the operations team of a large organization. The organization is running large-scale production apps in the cloud
You can then resolve the issues before they become severe.Logging and monitoring the health of your services helps you find the possible causes of failures and try to identify any problems before they occur.
Hence maintaing 

![](https://raw.githubusercontent.com/Ananyojha/spare-images/main/Aqua%20Music_20220206_172111_350.JPG)

### Azure Monitor
enables you to gather monitoring and diagnostic information about the health of your services. You can use this information to visualize and analyze the causes of problems that might occur in your app.

### Monitor
Sources of monitoring data from Azure applications can be organized into tiers, the highest tiers being your application itself and the lower tiers being components of Azure platform. 
[MS DOCS](https://docs.microsoft.com/en-us/azure/azure-monitor/agents/data-sources)

# key ability
Go to portal, explore yourself 

> All data collected by Azure Monitor fits into one of two fundamental types, metrics and logs.

### metrics and logs

### Metrics & logs

considered as the pillars of observability

Log -- Nothing new, every app generates logs 

Metric -- easy to view and find in a complex interconnected system compared to logs

### Data types 
Read slides 
----
### Activity log

-  Activity Logs record when resources are created or modified. Metrics tell you how the resource is performing and the resources it is consuming.
Entries in the Activity Log are system generated and cannot be changed

With the Activity Log, you can determine the ‘what, who, and when’ for any write operations (PUT, POST, DELETE) taken on the resources in your subscription

- Through activity logs, you can determine:

What operations were taken on the resources in your subscription?

✓ Who started the operation?

✓ When the operation occurred?

✓ The status of the operation.

✓ The values of other properties that might help you research the operation.

Log actual operation of the resources by enabling diagnostics and adding an agent to compute resources

> Let's go to portal, 

## Alerts
Show in portal + slides 

### log analytics
Log Analytics is a tool in the Azure portal used to edit and run log queries with data in Azure Monitor Logs
- it's built on top of Azure Data Explorer and uses the same Kusto Query Language (KQL). Log Analytics adds features specific to Azure Monitor such as filtering by time range and the ability to create an alert rule from a query. 

> From now slides + portal

### connected Services
- Collecting data into this platform allows data from multiple resources to be analyzed together using a common set of tools in Azure Monitor.
- `System Center Operations Manager (SCOM)` is a cross-platform data center monitoring system for operating systems and hypervisors.

[MS LEARN FROM HERE](https://docs.microsoft.com/en-us/learn/modules/configure-log-analytics/2-determine-uses)

### Extra knowledege
for automating general tasks in azure, we can create a automation account

> In Azure Automation, you can enable the Update Management, Change Tracking and Inventory, and Start/Stop VMs during off-hours features for your servers and virtual machines. These features have a dependency on a Log Analytics workspace, and therefore require linking the workspace with an Automation account. However, only certain regions are supported to link them together

- Azure Monitoring collects host-level metrics - like CPU utilization, disk and network usage - for all virtual machines without any additional software. For more insight into this virtual machine, you can collect guest-level metrics, logs, and other diagnostic data using the Azure Diagnostics agent. You can also send diagnostic data to other services like Application Insight

### Network Watcher 

[Refer to MS LEARN](https://docs.microsoft.com/en-us/learn/modules/configure-network-watcher/)
