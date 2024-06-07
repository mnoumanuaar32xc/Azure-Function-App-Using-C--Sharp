![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/5c2a4dd9-08ea-4063-b48d-96a43541d210)# Azure Function App Using C# 
  Create an Azure Function App Using C#

**What is Azure Functions**
  1. Serverless Services in Microsoft Azure   compariable to AWS/Lambda /Google Cloud Functions
  2. Event-driven serverless platform for problem solving
  3. Support various programming languages
  4. The Function App contains 1-n functions

**Follow the bellow steps for create a Azure Function App**
1. Click on create resource.
![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f4d8acba-eb17-407b-979e-950bbb073bb3)
2. search the Function App in search bar and click on create
3. select the hosting option as per your demand by default Consumptions are selected then click on select button 
   ![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/5849d582-d40c-4a50-81e3-210bdfafe810)
4. click on create new of resourse group ( Azure Subscriptions are a logical unit of Azure services that are linked to an Azure account. In order to take advantage of Azure's cloud-based services, you must have a subscription as it serves as a single billing unit for Azure resources used in that account)
   My Subscription Resourse group name is **Calculator**
   ![image](https://github.com/mnoumanuaar32xc/Azure-Function-App-Using-C--Sharp/assets/8413883/f0451131-4464-466b-a5cb-cc36640a299c)

   5. Function App name need to add global and unique functional App name that will be sub domain name for the .azurewebsites.net I will add **CalculatorWithAzure-func**
   6.  Publis on code
   7.  Runtime stack .Net
   8.  version 6 (End of Support Nov 8 2024 for dot net 6)
   9.  Region Weste Europe
   10.  click on Next Networking in Paid versions It shows Storage so you just create a storage account and chose the operating and chose the plan and click on Netx button
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














