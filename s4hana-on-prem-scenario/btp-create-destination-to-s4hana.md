## Connect SAP S/4HANA and SAP Task Center

Find information about the destination configuration that needs to be done for SAP Task Center in order to work with on-premise tasks from SAP S/4HANA on SAP BTP, Cloud Foundry environment.

### Prerequisites

* You have performed the steps in [Prepare SAP Cloud Connector and SAP S/4HANA](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/5c6cf3d9e754468fbd6b3f5073fe085f.html?version=latest) for the SAP Task Center Connection. *Choose your SAP S/4HANA version from the dropdown menu next to the documentation title*.

> ⚠ Caution -
For the setup of SAP Task Center, you must have a Cloud Connector that uses user UUID as the subject pattern for principal propagation. If you already have a Cloud Connector configuration that uses a different subject pattern (for example, e-mail), create a second Cloud Connector with user UUID and use it for the SAP Task Center communication.

* Make sure you save the following information, as you need it for the SAP S/4HANA destination setup:

    * **Location ID** from step Perform the initial configuration of the Cloud Connector and define location ID
    * **Virtual Host** and **Virtual Port** from step Configure access control in the Cloud Connector for your SAP S/4HANA system

* You have performed the steps in [SAP Task Center Integration](https://help.sap.com/viewer/0f18dddf28764f5b807ecd80549044cc/latest/en-US/1da230b82a984cda85d0041e13060a87.html) and have a user name and password for granting access to the task pull service, as described in [Create Service User for Task Pull Service](https://help.sap.com/viewer/0f18dddf28764f5b807ecd80549044cc/latest/en-US/229c5a1f659341efa2bb6205159d6209.html).

     Use the SAP Cloud Connector from the previous prerequisite for the step *Tunnel the request using, for example, the Cloud Connector* in [Configuring SAP Task Center Integration](https://help.sap.com/viewer/0f18dddf28764f5b807ecd80549044cc/latest/en-US/5117f21ef28f4e698d99fe3fdbc1be2a.html).

* You have the client number of your SAP S/4HANA system.

* You have completed all prerequisites for the initial setup.

ℹ Do not configure more than one destination to the same SAP S/4HANA system for one SAP Task Center. This will result in having duplicate tasks for end users 

1. Navigate to the subaccount on SAP Business Technology Platfrom, where your SAP Task Center instance was created, and select the **Destinations** tab from the navigation area on the left.

2. If you have executed the automatic setup , you already have a sample destination called S4HANA. You can use the sample destination or clone it, and update the properties as described below.

    If you have followed the manual setup (see Manual Setup), you have to create a new destination and manually add the properties as described below.

3. Configure the properties of the destination as follows:
    
    | Property | Description | Example or Value
    |---|---|---
    | **Name** | Configure a destination name. It can be up to 16 characters long. ℹ *The name of the destination must not be longer than 16 characters, otherwise the status of the respective SAP Task Center connector will be set to Error.* | **Example**: S4HANA
    | **Type** | Choose the HTTP option from the dropdown menu. |
    | **Description** | (Optional) Add a description. |
    | **URL** | Create the URL by following the pattern \<Virtual Host>:\<Virtual Port>, using the values you've got when configuring the access control in the SAP Cloud Connector. For more information, see *Prerequisites*. |
    | **Proxy type** | Choose the **OnPremise** option from the dropdown menu. |
    | **Authentication** | Choose the **BasicAuthentication** option from the dropdown menu. |
    | **User** | Add the service user for task pull service. For more information, see *Prerequisites*. |
    | **Password** | Add the password for the service user for task pull service. For more information, see *Prerequisites*. |
    | **Location ID** | Provide the **Location ID** that you configured in the initial configuration of the SAP Cloud Connector. For more information, see *Prerequisites*. |
    

    **Addtional Properties**:
    
    | Property | Description | Example or Value
    |---|---|---
    | **tc.enabled** | Enables the SAP Task Center to connect to the configured task provider destination. | **Value**: true
    | **tc.provider_type** | Type of the task provider. | S/4HANA
    |**tc.ui.group** and **tc.ui.group.[language_code]** | For more information, see C[onfigure Filter Tabs in the SAP Task Center Web App](). | **Example**: SAP S/4HANA 
    | URL.queries.sap-client | The client number of the SAP S/4HANA system. | **Example**: 100

4. Save your configuration.

![BTP destination set up](images/btp_s4h_destination.png)

> ℹ If you choose **Check Connection** in the destination configuration, you may not receive correct information about the connectivity between the SAP Task Center service and SAP S/4HANA 


