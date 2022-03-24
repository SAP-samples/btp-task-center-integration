Introduction

In order to use SAP Task Center with SAP S/4HANA Cloud, it's important that the S/4AHANA Cloud user profile has the **Global User ID** populated with a value that matches the **User UUID** field from the user profile in SAP Cloud Identity Authentication Service(IAS).  This field will normally be empty after users are onboarded in SAP S/4HANA Cloud.  For more ifnormation on S/4HANA Cloud user onboarding process, refere the links below:
https://blogs.sap.com/2017/12/07/sap-s4hana-cloud-system-setup/
https://microlearning.opensap.com/media/User+Management+Overview+-+SAP+S+4HANA+Cloud+Deployment/1_26wlxfj9

Now that we know why we need to do this, let’s look at the mechanics of how to use SAP Cloud Identity Provisioning Service (IPS) to replicate the users from SAP Cloud Identity Authentication Service (IAS) to SAP S/4HANA Cloud.  Following steps are required to provision users:

Create a Communication System in S/4HANA Cloud
Setup IAS as a source system in IPS
Setup SAP S/4HANA Cloud as a target system in IPS
Run the source provisioning job

Create a Communication System in S/4HANA Cloud

Log into your S/4HANA Cloud system and access Maintain Communication Users.
Click New and create a new communication user.  Specify a User Name, Description, and Password.  Click Create.
Access Communication Systems.
Click New and specify a System ID and System Name and click Create.
Specify a value for Host Name to match your IAS tenant hostname.  For eg. xxxxxxx.accounts.ondemand.com
Click + under Users for Inbound Communication.
Select the Communication user created earlier and click OK.
Save your Communication System.
Access Communication Arrangements
Click New and choose the value help icon to open up the list of available communication scenarios.
Search for SAP_COM_0193 and select it from the list.  This communication scenario is relevant for Identity Provisioning integration.
Specify a name for the arrangement and click Create.
Use the value help icon and select the Communication System created earlier.  The User Name for inbound communication should automatically populate.  Save your configuration.
Setup IAS as a source system in IPS

Access your IAS Administration Console.
Under Administrators, click Add >> System.
Specify a name for your user and ensure the following authorizations are enabled:
Manage Users
Manage Groups
Manage Tenant Configuration
For Set Password section, click Not Configured.
Specify a password for your user and click Save.  After saving, you will redirected back to the previous screen.  Navigate back to the password screen and copy the User ID using the Copy icon.  We need this User ID and the password later when setting up IAS as a source system in IPS.
Access your SAP Cloud Identity Services – Identity Provisioning (IPS) tenant.
Click on Source Systems.
Click Add.
Specify the following and click Save:
Type: Identity Authentication
System Name: <name of your choice>
Click Properties. You will see a list of pre-created properties.
Click Add to add new properties.  Use the Standard option for non-sensitive properties and Credential option for password fields.
Add the additional properties below and click Save. Take a look at the help guide for the complete list of properties that are possible with Identity Authentication as a target system.
Type: HTTP
ProxyType: Internet
URL: <your IAS tenant URL>
Authentication: BasicAuthentication
User: <IAS system user>
Password: <IAS system user password>
Screenshot below shows the setup of my source job setup in IPS.  Notice that I’ve also added some additional properties to filter the user and group that is read from IAS.  It’s good idea to test the provisioning job with couple users and groups before you remove the filter and run the job for all users and groups.  For the purpose of this blog, I am just going to provision the “DEMO” user and “BR_DEMO” group.



Setup SAP S/4HANA Cloud as a target system in IPS

Access your SAP Cloud Identity Services – Identity Provisioning (IPS) tenant.
Click the Target System icon and click Add.
Specify the following and click Save:
Type: SAP S/4HANA Cloud
System Name: <name of your choice>
Source System: <your IAS source system created earlier>
Under Properties, add the additional properties below and click Save. Take a look at the help guide for the complete list of properties that are possible with S/4HANA Cloud as a target system.
Type: HTTP
ProxyType: Internet
URL: <S4/HANA Cloud URL>
Authentication: BasicAuthentication
User: <Communication User created in S/4 system earlier>.
Password: <Password of the communication user>
The screenshot below shows the setup of my target system in IPS.



Run the source provisioning job

Switch to Source Systems.
Select your source job and click Jobs icon.  Click Run Now icon to start the Read Job.
Monitor the status of your job under the Job Logs until you see a Success or Failure status.  You will need to navigate away and come back to this page to see the updated status.
View the details of the job execution.  In my case 1 users and 1 group is created successfully.
Once the provisioning job is successfully executed, the demo user in S/4 system has the Global User ID and Business Role assigned.



 

While the focus of this blog is on S/4HANA Cloud, majority of the steps covered here can easily be adapted to provision users to other ABAP based cloud systems, such as: SAP Integrated Business Planning (IBP) and SAP BTP ABAP Environment.
