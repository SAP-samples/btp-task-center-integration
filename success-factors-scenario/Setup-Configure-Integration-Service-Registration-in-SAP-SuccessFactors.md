To configure the Integration Service Registration, get the service key from your SAP BTP global account to use it for the registration in SAP SuccessFactors.

Step 1: Get the Service Key for SAP Task Center from SAP BTP subaccount:

Logon to the SAP BTP Cockpit and navigate to your subaccount. Choose **Instances and Subscriptions**. Choose **Instances** tab. 

![alt text](images/1.png)

To download the service key credential, choose the key as shown in previous screenshot.
Open the Service key file you downloaded and note the following values which you need in Step 2 of configuration below:
**Endpoints**->  inbox_rest_url
**uaa**->url
**uaa**->  clientid
**uaa**-> clientsecret

Step 2: Configure SAP SuccessFactors Registration

Logon to the **SAP SuccessFactors** system with admin user and go to **Admin Center**.
Search for **Integration Service Registration Center**.
From the Integration Service dropdown list, choose **Task Center**.
Enter data with the values which you copied from service key file previously:
**Destination URL**: inbox_rest_url (NOTE: Remove everything that comes after ".com".)
**OAuth URL**: url (NOTE: append /oauth/token after ".com")
**Client ID**: clientid
**Client Secret**: clientsecret
Choose **Register**.

![alt text](images/2.png)