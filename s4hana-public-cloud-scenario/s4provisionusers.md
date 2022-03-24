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

1. Log into SAP S/4HANA Cloud system and access **Maintain Communication Users**.
2. Click **New** and create a new communication user.
3. Specify a **User Name**, **Description**, and **Password**.
4. Click **Create**.
5. Access **Communication Systems**.
6. Click **New** and specify a **System ID** and **System Name** and click **Create**.
7. Specify a value for **Host Name** to match your IAS tenant hostname. For eg. **xxxxxxx.accounts.ondemand.com**
8. Click **+** under Users for Inbound Communication.
9. Select the Communication user created earlier and click **OK**.
10. Save your Communication System.
11. Access **Communication Arrangements**.
12. Click **New** and choose the value help icon to open up the list of available communication scenarios.
13. Search for **SAP_COM_0193** and select it from the list. This communication scenario is relevant for Identity Provisioning integration.
14. Specify a name for the arrangement and click **Create**.
15. Use the value help icon and select the Communication System created earlier. The User Name for inbound communication should automatically populate. **Save** your configuration.

### Setup SAP Cloud Identity Authentication Service(IAS) as a source system in SAP Cloud Identity Provisioning Service(IPS)

1. Access your IAS Administration Console.
2. Under Administrators, click **Add >> System**.
3. Specify a name for your user and ensure the following authorizations are enabled:
   * __Manage Users__
   * __Manage Groups__
   * __Manage Tenant Configuration__
4. For **Set Password** section, click **Not Configured**.
5. Specify a password for your user and click **Save**.  After saving, you will redirected back to the previous screen. Navigate back to the password screen and copy the **User ID** using the Copy icon.
7. Access SAP Cloud Identity Provisioning (IPS) tenant.
8. Click on **Source Systems**.
9. Click **Add**.
10. Specify the following and click **Save**.
    * __Type__: Identity Authentication
    * __System Name__: Name of your choice
11. Click **Properties** to open up the list of pre-created properties.
12. Click **Add** to add new properties. Use the Standard option for non-sensitive properties and Credential option for password fields.
13. Add the additional properties below and click Save.
    * __Type__: HTTP
    * __ProxyType__: Internet
    * __URL__: SAP Cloud Identity Authentication Service tenant URL
    * __Authentication__: BasicAuthentication
    * __User__: System user created in IAS earlier
    * __Password__: Password for the system user
    
### Setup SAP S/4HANA Cloud as a target system in SAP Cloud Identity Provisioning Service(IPS)
1. Access SAP Cloud Identity Provisioning (IPS) tenant.
2. Click the **Target System** icon and click **Add**.
3. Specify the following and click Save:
   * __Type__: SAP S/4HANA Cloud
   * __System Name__: Name of your choice
   * __Source System__: Identity Authentication source system created earlier
 4. Click **Properties** to open up the list of pre-created properties.
 5. Click **Add** to add new properties. Use the Standard option for non-sensitive properties and Credential option for password fields.
 6. Add the additional properties below and click **Save**.
    * __Type__: HTTP
    * __ProxyType__: Internet
    * __URL__: S/4HANA Cloud URL
    * __Authentication__: BasicAuthentication
    * __User__: Communication User created in S/4 system earlier
    * __Password__: Password for communication user
  
### Run the source provisioning job
1. Switch to **Source Systems*8. 
2. Select your source job and click **Jobs** icon. 
3. Click **Run Now** icon to start the **Read** Job.
4. Under **Job Logs** monitor the status until you see a **Success** status.  You will need to navigate away and come back to this page to see the updated status.
5. View the details of the job execution and confirm users were provisioned successfully.
6. Log into your S/4 system, and confirm the **Global User ID** is populated for the business users.
