# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

*For this Article CMS Web App, I chose an Azure App Service instead of an Azure VM, becuase Azure App Service is basically a PaaS that provides adeqaute platform a web app to run whereas VM is a IaaS that increases responsibilities from application runtime to OS level that are not applications responsibilities.*

*In terms of cost, this app run is still in DEV environment, so I chose basic free tier dev/test plan that provides 1 GB of memory adequate enough to test the web app. When we move to the production app, there are multiple pricing tiers are available to choose and will be decided based on the user growth of the app*

*In term of scalability and availability, the app runs on a single instance at only one region to reduce dev/test costs. If the app deployed to the production environment, we can choose horizontal scaling or auto-scaling when there is a demand increases that creates/terminates VM resources that are automated by Azure. We can also use vertical scaling to increase the performance of the app running in a single VM.*

*For the workflow, the web app CI/CD can be leveraged by using azure github actions and several other options available that builds, deploys, and runs the web app instances on the running VMs automatically whenever we commit any change to the remote repository.*


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

*If the web app needs more control over which OS it needs to run and also if we want to manage it ourself to make our own customized environment including runtime, middleware, custom OS, own security model or softwares, etc for the app to run on. But for this article cms web app, the Azure App Service would be the most suitable option in terms of cost and maintenance.
