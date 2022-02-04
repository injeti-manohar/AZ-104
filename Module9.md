# PaaS compute Resource



## App service Plan

- defines a set of compute resources for a web app to run. These compute resources are just like the server farm in traditional web hosting. I.e  One or more apps can be configured to run on the same computing resources (or in the same App Service plan).
- just like your wifi plan, buy plan --> run diff. devices (& diff Applications) --> all share same source of power (wifi router)
--------------------
|______ apps_______|
<Br>
|__________________ plan (arranges required compute, network,storage etc)_________|


- It creates VM's behind the scene. 
- If the plan is configured to run five VM instances, then all apps in the plan run on all five instances. If the plan is configured for autoscaling, then all apps in the plan are scaled out together based on the autoscale settings.
- If you enable diagnostic logs, perform backups, or run WebJobs, they also use CPU cycles and memory on these VM instances

> Create app service plan in Portal

**Best Practices** - 
- deploy your apps in same app service plan, as long as demand is met

Isolate your app into a new App Service plan when:

- The app is resource-intensive.
- You want to scale the app independently from the other apps in the existing plan.
- The app needs resource in a different geographical region 


## App Services 

Azure App Service brings together everything you need to create websites, mobile backends, and web APIs for any platform or device. Applications run and scale with ease on both Windows and Linux-based environments. There are many deployment choices. ⏬
![Different Hosting Options in App Service](https://docs.microsoft.com/en-us/learn/wwl-azure/configure-azure-app-services/media/web-quickstarts-c154c8e4.png)

> Go to portal to explore and explain about Azure App Service


**Reasons for choosing App Services**
- Developer friendly : choose any language, framework well integrated with VS CODE and Visual Studio
- Devops Optimised : set up CI/CD with Azure DevOps, GitHub, BitBucket, Docker Hub, or Azure Container Registry. Promote updates through test and staging environments. Manage your apps in App Service by using Azure PowerShell or the cross-platform command-line interface (CLI).
- Various Connectors like : (such as SAP), SaaS services (such as Salesforce), and internet services (such as Facebook). Access on-premises data using Hybrid Connections and Azure Virtual Networks.

- [Ms Learn -- Create App Service](https://docs.microsoft.com/en-us/learn/modules/configure-azure-app-services/3-create-app-service)

- [Learn more in MS Product Page](https://azure.microsoft.com/en-in/services/app-service/)

------
#### Application Insights 
Application Insights, a feature of Azure Monitor, monitors your live applications

.-----

## Lesson 2 : Container Services

### Container Vs VM 

**Why Containers ?**
A container is essentially a package that contains everything that is needed to execute a piece of software. The package includes:

- The application executable code.
- The runtime environment (such as .NET Core).
- System tools.
- Settings.

✓ each container shares the same host OS or system kernel and is much lighter in size, often only megabytes. This often means a container might take just seconds to start (versus the gigabytes and minutes required for a typical VM

> Example -- DOCKER, LXD, PODMAN 

#### Container Architecture -- 
![](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/media/container-diagram.svg)

#### VM Architecture -- 
![](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/media/virtual-machine-diagram.svg)

- [MS DOCS](https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/containers-vs-vm)

### Azure Container Instances

[Read from MS LEARN](https://docs.microsoft.com/en-us/learn/modules/configure-azure-container-instances/3-review)

### Azure Container Groups 
A container group is a collection of containers that get scheduled on the same host machine. The containers in a container group share a lifecycle, resources, local network, and storage volumes. It's similar in concept to a pod in Kubernetes.

> Common use cases described in [MS LEARN](https://docs.microsoft.com/en-us/learn/modules/configure-azure-container-instances/4-implement-container-groups)

### Docker
The software can be developed locally within a Docker container, shared with Quality Assurance resources for testing. and then deployed to production in the Azure Cloud. Once deployed, the application can easily be scaled using the Azure Container Instances (ACI).

## lesson 3 AKS
The standard container management runtime focuses on managing individual containers. If you want to scale a complex system with multiple containers working together, this scenario becomes challenging. To make the management process easier, it's common to use a container management platform, such as Kubernetes.

### terminology
- Pools are groups of nodes with identical configurations.

- Nodes are individual virtual machines running containerized applications.

- Pods are a single instance of an application. A pod can contain multiple containers.

- Container is a lightweight and portable executable image that contains software and all of its dependencies.

- Deployment has one or more identical pods managed by Kubernetes.

- Manifest is the YAML file describing a deployment.
