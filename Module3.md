your application is typically made up of many components – maybe a virtual machine, storage account, and virtual network, or a web app, database, database server, and third-party services. 
So with ARM You can deploy, update, or delete all the resources for your solution in a single, coordinated operation. You use a template for deployment and that template can work for different environments such as testing, staging, and production


### ARM
Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features, like access control, locks, and tags, to secure and organize your resources after deployment

- Resource Manager receives the request. It authenticates and authorizes the request **RBAC also uses ARM to authorise**
Manage your infrastructure through declarative templates rather than scripts.

Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.

Redeploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.

Define the dependencies between resources so they're deployed in the correct order.

> declarative syntax - Syntax that lets you state "Here is what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure

## terminology

`Resouces provider ` -- Microsoft.Compute, which supplies the virtual machine resource, Microsoft.Storage, which supplies the storage account resource

### Resource Groups
- All the resources in your resource group should share the same lifecycle. 
- You can move a resource from one resource group to another group. For more information, 
- immutable deployments are not supported in a resource group. 
- No limit for Resouces -- Deployments are incremental; if a resource group contains two web apps and you decide to deploy a third, the existing web apps will not be removed
> You may be wondering, "Why does a resource group need a location? And, if the resources can have different locations than the resource group, why does the resource group location matter at all?"

The resource group stores metadata about the resources. When you specify a location for the resource group, you're specifying where that metadata is stored. For compliance reasons, you may need to ensure that your data is stored in a particular region.

Except in global resources like Azure Content Delivery Network, Azure DNS, Azure Traffic Manager, and Azure Front Door, if a resource group's region is temporarily unavailable, you can't update resources in the resource group because the metadata is unavailable. The resources in other regions will still function as expected, but you can't update them

- You can apply tags to a resource group. The resources in the resource group don't inherit those tags.

## Resource Locks
The power of azure lies also the ease with which they can be deleted. An over-zealous or careless administrator can accidentally erase months of work with a few steps. Resource Manager locks allow organizations to put a structure in place that prevents the accidental deletion of resources in Azure.

## resource limits
[Check your limits through Microsoft website](https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits?toc=%2fazure%2fnetworking%2ftoc.json)

- The limits shown are the limits for your subscription.
- When you need to increase a default limit, there is a Request Increase link.
- All resources have a maximum limit listed in Azure limits.
- If you are at the maximum limit, the limit can't be increased.
