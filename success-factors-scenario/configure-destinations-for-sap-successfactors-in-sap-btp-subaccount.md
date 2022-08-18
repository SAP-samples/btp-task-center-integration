In this section, you configure 2 destinations in your SAP BTP subaccount for SAP SuccessFactors. For this configuration, you export your trust certificate and register the client application. The 2 destinations are:

- Primary Destination: Create a primary destination with the technical user, as described in ["Creating the Primary Destination with the Technical User"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/dc5407b42c7e435b8124ee7a0816249c.html).
- Secondary Destination: Create a secondary destination for principal propagation, as described in ["Creating a Secondary Destination for the Principal Propagation"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/bf657f8adefa4a468aa3c71783fca291.html).

Step 1: Save the trust certificate locally

- To export the trust certificate which you need for registering your client, follow below steps: 
- Logon to SAP BTP and navigate to the subaccount, where your SAP Task Center instance was created. 
- From the navigation pane, choose Connectivity -> Destinations.
- Choose Download Trust.
- Save the trust certificate file locally.
For additional information refer to ["Connect SAP SuccessFactors and SAP Task Center"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/eae23f3a679d481295ff05bdb322f859.html).

Step 2: Register the OAuth Client Application in SAP SuccessFactors to generate the API key which is needed to configure the destination

- Logon to the SAP SuccessFactors system.
- Go to **Admin Center -> Manage OAuth2 Client Applications**.
- Choose **Register Client Application**.
- Enter data as shown in step 2 of Procedure section of the document: ["Creating the Primary Destination with the Technical User"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/dc5407b42c7e435b8124ee7a0816249c.html).
- Save your changes.
- To open the registered application, choose View. Copy API KEY value. 
- Open the downloaded Service Key file and note the following values: 
    - endpoints  inbox_rest_url
    - uaa  url
    - uaa  clientid
    - uaa  clientsecret

Step 3: Configure the primary destination (using technical User)

- Logon to SAP BTP and navigate to your SAP BTP Subaccount.
- Choose **Connectivity** -> **Destinations**.
- Note that if you have used automatic setup in SAP BTP with a booster, you see destination template with the name Success_Factors is already created. You can configure this destination as a primary destination by updating all the properties as described in step 3 below. However, If you have followed the manual setup (see ["Manual Setup"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/0f00d3d3e2ab460c856d409c469fb4f1.html)), create a new destination and manually add the properties as described in step 3:
["Creating the Primary Destination with the Technical User - SAP Help Portal"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/dc5407b42c7e435b8124ee7a0816249c.html)
- In the **Destination Configuration** pane , choose **new property**.
- Add the properties as mentioned under step 4 of ["Creating the Primary Destination with the Technical User - SAP Help Portal"](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/dc5407b42c7e435b8124ee7a0816249c.html)
- Make sure the **tc.enabled** property with the value true has been added manually for the Primary SuccessFactors destination.

Step 4: Configuration of the secondary destination (Principal Propagation)

- Follow the steps mentioned in ["Creating a Secondary Destination for the Principal Propagation - SAP Help Portal" ](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/bf657f8adefa4a468aa3c71783fca291.html).