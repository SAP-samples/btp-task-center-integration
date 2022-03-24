### Introduction

In order to use SAP Task Center with SAP S/4HANA Cloud, it's important that the S/4AHANA Cloud user profile has the **Global User ID** populated with a value that matches the **User UUID** field from the user profile in SAP Cloud Identity Authentication Service(IAS).
<img alt="update2" src="Update2.png"/>
This field will normally be empty after users are onboarded in SAP S/4HANA Cloud. For more information on S/4HANA Cloud user onboarding process, refer to the links below:
* https://blogs.sap.com/2017/12/07/sap-s4hana-cloud-system-setup/
* https://microlearning.opensap.com/media/User+Management+Overview+-+SAP+S+4HANA+Cloud+Deployment/1_26wlxfj9

To populate the Global User ID field in S/4HANA Cloud user profile we need to use SAP Cloud Identity Provisioning Service (IPS) to replicate the users from SAP Cloud Identity Authentication Service(IAS) to SAP S/4HANA Cloud.
* Create a Communication System in S/4HANA Cloud
* Setup SAP Cloud Identity Authentication Service(IAS) as a source system in SAP Cloud Identity Provisioning Service(IPS)
* Setup SAP S/4HANA Cloud as a target system in SAP Cloud Identity Provisioning Service(IPS)
* Run the source provisioning job

### Create a Communication System in SAP S/4HANA Cloud

1. Log into SAP S/4HANA Cloud system and access Maintain Communication Users.
2. Click New and create a new communication user.
3. Specify a User Name, Description, and Password.
4. Click Create.
5. Access Communication Systems.
6. Click New and specify a System ID and System Name and click Create.
7. Specify a value for Host Name to match your IAS tenant hostname. For eg. xxxxxxx.accounts.ondemand.com
8. Click + under Users for Inbound Communication.
9. Select the Communication user created earlier and click OK.
10. Save your Communication System.
11. Access Communication Arrangements.
12. Click New and choose the value help icon to open up the list of available communication scenarios.
13. Search for SAP_COM_0193 and select it from the list. This communication scenario is relevant for Identity Provisioning integration.
14. Specify a name for the arrangement and click Create.
15. Use the value help icon and select the Communication System created earlier. The User Name for inbound communication should automatically populate. Save your configuration.

### Setup SAP Cloud Identity Authentication Service(IAS) as a source system in SAP Cloud Identity Provisioning Service(IPS)

1. Access your IAS Administration Console.
2. Under Administrators, click Add >> System.
3. Specify a name for your user and ensure the following authorizations are enabled:
   * Manage Users
   * Manage Groups
   * Manage Tenant Configuration
For Set Password section, click Not Configured.
4. Specify a password for your user and click Save. After saving, you will redirected back to the previous screen. Navigate back to the password screen and copy the User ID using the Copy icon. We need this User ID and the password later when setting up SAP Cloud Identity Authentication Service as a source system in SAP Cloud Identity Provisioning Service.
5. Access SAP Cloud Identity Provisioning (IPS) tenant.
6. Click on Source Systems.
7. Click Add.
8. Specify the following and click Save:
   * Type: Identity Authentication
   * System Name: Name of your choice
9. Click Properties. You will see a list of pre-created properties.
10. Click Add to add new properties. Use the Standard option for non-sensitive properties and Credential option for password fields.
11. Add the additional properties below and click Save.
    * Type: HTTP
    * ProxyType: Internet
    * URL: SAP Cloud Identity Authentication Service tenant URL
    * Authentication: BasicAuthentication
    * User: System user created in step 3
    * Password: Password for the system user

###Setup SAP S/4HANA Cloud as a target system in SAP Cloud Identity Provisioning Service(IPS)
1. Access SAP Cloud Identity Provisioning (IPS) tenant.
2. Click the Target System icon and click Add.
3. Specify the following and click Save:
   * Type: SAP S/4HANA Cloud
   * System Name: Name of your choice
   * Source System: Identity Authentication source system created earlier
 4. Click Properties. You will see a list of pre-created properties.
10. Click Add to add new properties. Use the Standard option for non-sensitive properties and Credential option for password fields.
11. Add the additional properties below and click Save.
    * Type: HTTP
    * ProxyType: Internet
    * URL: S4/HANA Cloud URL
    * Authentication: BasicAuthentication
    * User: Communication User created in S/4 system earlier
    * Password: S4/HANA Cloud URL
  
Run the source provisioning job

Switch to Source Systems. Select your source job and click Jobs icon. Click Run Now icon to start the Read Job. Monitor the status of your job under the Job Logs until you see a Success or Failure status. You will need to navigate away and come back to this page to see the updated status. View the details of the job execution. In my case 1 users and 1 group is created successfully. Once the provisioning job is successfully executed, the demo user in S/4 system has the Global User ID and Business Role assigned.

While the focus of this blog is on S/4HANA Cloud, majority of the steps covered here can easily be adapted to provision users to other ABAP based cloud systems, such as: SAP Integrated Business Planning (IBP) and SAP BTP ABAP Environment.
