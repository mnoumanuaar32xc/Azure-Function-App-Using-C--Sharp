# Azure Function App Using C# with Example Calculator
 An Azure Function App has been created. Let's explore the process of building, configuring, and executing a function within this app.
 Specifically, we will create a Calculator Function as part of this Function App.
 

# What is Azure Functions
  1. Serverless Services in Microsoft Azure   compariable to AWS/Lambda /Google Cloud Functions
  2. Event-driven serverless platform for problem solving
  3. Support various programming languages
  4. The Function App contains 1-n functions
# Why use Azure Functions
Azure Functions is a serverless compute service that enables you to run event-driven code without having to explicitly provision or manage infrastructure. Here are five points about why Azure Functions are beneficial, along with examples:
Summarized Examples:
1. **Cost-Effective**: Automatically scaling notifications for an e-commerce site.
2. **Simplified Development**: A Python function processing data in Azure Blob Storage.
3. **Event-Driven Execution**: Sending welcome emails via Azure Queue Storage triggers.
4. **Microservices Architecture**: Modular functions handling separate services in a web app.
5. **Monitoring and Analytics**: Real-time monitoring of data processing functions with Azure Application Insights.
 
**Follow the bellow steps for create a Azure Function App**
1. Click on create resource.
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f4d8acba-eb17-407b-979e-950bbb073bb3)
2. search the Function App in search bar and click on create
  4. select the hosting option as per your demand by default Consumptions are selected then click on select button

  **Choose a service plan**
Function apps may use one of the following hosting plans:

**Consumption plan
Premium plan
Dedicated (App service) plan**
When using the Azure serverless application platform, choose the Consumption plan. This plan provides automatic scaling and bills you only when your functions are running. The **Consumption** plan comes with a configurable timeout period for executing a function. By default, it's five (5) minutes, but may be configured to have a timeout as long as 10 minutes.

The **Premium plan** also dynamically scales your resources to meet demand, but you can specify a minimum number of VM instances to keep warm and reduce so called "cold starts." The Premium plan also lets your functions connect to and run inside virtual networks. Like the Dedicated plan, the default timeout for apps in a Premium plan is 30 minutes, but they can essentially run for an unlimited time (depending on server availability).

**The Dedicated (App service)** plan enables you to avoid timeout periods by having your function run continuously on a VM that you define. An App service plan is technically not a serverless plan, because you're responsible for managing the app resources the function runs on. However, it may be a better choice when you already have excess App Service resources available on which to also run your functions.

   ![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/5849d582-d40c-4a50-81e3-210bdfafe810)
6. click on create new of resourse group ( Azure Subscriptions are a logical unit of Azure services that are linked to an Azure account. In order to take advantage of Azure's cloud-based services, you must have a subscription as it serves as a single billing unit for Azure resources used in that account)
   My Subscription Resourse group name is **Calculator**
   ![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f0451131-4464-466b-a5cb-cc36640a299c)

   5. Function App name need to add global and unique functional App name that will be sub domain name for the .azurewebsites.net I will add **CalculatorWithAzure-func**
   6.  Publis on code
   7.  Runtime stack .Net
   8.  version 6 (End of Support Nov 8 2024 for dot net 6)
   9.  Region Weste Europe
   10.  click on Next Networking in Paid versions It shows Storage so you just create a storage account and chose the operating and chose the plan and click on Netx button
  **Storage account requirements**
  When you create a function app, it must be linked to a storage account. You can select an existing account or create a new one. The function app uses this storage account for internal   operations, such as logging function executions and managing execution triggers. On the Consumption plan, this storage account is also where the function code and configuration file are stored.

   11. Next is Networking (Networkig is not avaliable for azure function so that use the consumption plan click on netx button Monitoring Tab will be appear) click on Enable insight No
   12. click on next > Deployment click on Next Tags without any setting and then next click Next> review +create

       ![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/474de002-32b4-4cd0-b4e8-f2636f60f3f0)
   13. All configuration will be appera you can download all configuration
   14. then click on Create button after some time Function App will be created
   
   **Create azure function App in VisualStudio** 

open the Visual Studio I am using 2022 and create new project and Search **Azure Function** if you don't have Azure Function Ist update your Visual Studio
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f8fc5d61-8687-433a-94be-1ad72b5c02c8)
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/88bae070-fe1c-4fb9-80f6-f62e2ae23497)
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/c07063f9-d743-40f7-a785-11fbb0c16a20)
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/0ba2c516-9bb3-490a-946e-c5ee4f0e5255)

after project creating take a look properties of the project
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/e7c17cae-1be7-4ee5-abec-141c3e76be8a)
view the Nuget packages
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/dae2cbde-1fae-49c2-a59a-6af2a5a456f4)
see the Function1.cs class
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/ee2f62cb-3e1d-4b9c-ae36-b8a12e12c05b)
Change the Class Name and implement the logic and run the Application
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/59b199a9-ec6f-40f1-862c-3d835d1265cc)
output
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/3302a610-afbc-40a2-9856-a32917ac751d)
After run the application you will see the Consol Windown where a Function End URL will be mention 
lets try in browser :- http://localhost:7269/api/Sum?x=10&y=10
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/41f99f33-bf4e-4142-94cb-62d7ff3bbad9)
and in consol window you will also see the Http Trigger function proceed request summery 
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f9486290-eb6f-4724-b2e2-4806e381df7f)

**Deploy the function app inthe Azure**
Project + publish 
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/76be30b4-3eac-4de1-bf8a-4f54fcddffa1)
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/2384e6a8-38cc-4035-b671-a06d7842dff5)
After Next Make Sure you are SignIn with your Azure Login Account , then Search your Function and select it , at the End Checked the check box.and Finish

![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/8e7093bd-d908-4f02-bb04-e0f9d324e937)
and click on Publish Button
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/839e83d6-b8ed-4c4c-a777-1f3c518d7917)
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/595fbba9-9025-4f0c-a99c-c683e4498435)

Go back to https://portal.azure.com/ 

click on your Function CalculatorWithAzure-func scroll down check your Function Class Sum and Click 

![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/5dd4604e-f4e6-41b3-8f5b-cb8e3f082d5b)

get the URl from Get Function URl and redesign your URL with Parameters 
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/12b39c2a-3d6e-477c-917f-ab3656908c34)

Output of Azure Function URl 
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/703d3edd-4d94-401d-9f97-a8d4ee691e91)


End Test your URL as bellow 

https://calculatorwithazure-func.azurewebsites.net/api/Sum?x=100&y=10&code=ltvfazHLKrR2Skm4lG31KsTu7i3aWHRxVbUNHEcmrkjZAzFuAbiu1w%3D%3D


**Next we will Triggers and bindings**










