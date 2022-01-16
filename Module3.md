### ARM
Azure Resource Manager is the deployment and management service for Azure. It provides a management layer that enables you to create, update, and delete resources in your Azure account. You use management features, like access control, locks, and tags, to secure and organize your resources after deployment

- Resource Manager receives the request. It authenticates and authorizes the request **RBAC also uses ARM to authorise**
Manage your infrastructure through declarative templates rather than scripts.

Deploy, manage, and monitor all the resources for your solution as a group, rather than handling these resources individually.

Redeploy your solution throughout the development lifecycle and have confidence your resources are deployed in a consistent state.

Define the dependencies between resources so they're deployed in the correct order.

> declarative syntax - Syntax that lets you state "Here is what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure

### Resource Groups
- All the resources in your resource group should share the same lifecycle. 
- You can move a resource from one resource group to another group. For more information, see Move resources to new resource group or subscription
> You may be wondering, "Why does a resource group need a location? And, if the resources can have different locations than the resource group, why does the resource group location matter at all?"

The resource group stores metadata about the resources. When you specify a location for the resource group, you're specifying where that metadata is stored. For compliance reasons, you may need to ensure that your data is stored in a particular region.

Except in global resources like Azure Content Delivery Network, Azure DNS, Azure Traffic Manager, and Azure Front Door, if a resource group's region is temporarily unavailable, you can't update resources in the resource group because the metadata is unavailable. The resources in other regions will still function as expected, but you can't update them

- You can apply tags to a resource group. The resources in the resource group don't inherit those tags.
