# What's this

This sample is from Abp vNext framework to demonstrate how to use abp to construct a microservice solution.
If you follow the official [documentation](https://abp.io/documents/abp/latest/Samples/Microservice-Demo) to download the latest code to run the demo, it may be not work, no matter use docker or run it from the source code.

So I spent some time to find the issues and fixed them. Now you can clone this repo to run in the local machine directly.

# Steps to run
## Pre Requirements
To be able to run the solution from source code, following tools should be installed and running on your computer:

* SQL Server 2015+ (can be express edition)
* Redis 5.0+
* RabbitMQ 3.7.11+
* MongoDB 4.0+
* ElasticSearch 6.6+
* Kibana 6.6+ (optional, recommended to show logs)

## Create Databases
**I Updated the default db from SqlServer to MySql**
### MsDemo_Identity Database
1. Right click to the AuthServer.Host project and click to the Set as startup project.
2. Open the Package Manager Console (Tools -> Nuget Package Manager -> Package Manager Console)
3. Select AuthServer.Host as the Default project.
4. Run Update-Database command.

### MsDemo_ProductManagement
1. Right click to the ProductService.Host project and click to the Set as startup project.
2. Open the Package Manager Console (Tools -> Nuget Package Manager -> Package Manager Console)
3. Select ProductService.Host as the Default project.
4. Run Update-Database command.

## Run Projects

Run the projects with the following order (right click to each project, set as startup project an press Ctrl+F5 to run without debug)

* AuthServer.Host
* IdentityService.Host
* BloggingService.Host
* ProductService.Host
* InternalGateway.Host
* BackendAdminAppGateway.Host
* PublicWebSiteGateway.Host
* BackendAdminApp.Host
* PublicWebSite.Host
* When you run projects, they will add some initial demo data to their databases.