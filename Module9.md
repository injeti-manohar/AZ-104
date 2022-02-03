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
