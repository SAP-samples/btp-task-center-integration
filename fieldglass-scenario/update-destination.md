1. Navigate to the Cloud Foundry subaccount, where your SAP Task Center instance was created, and select the **Connectivity** > **Destinations** tab from the navigation area on the left.  
2. Under **Destinations**, select the **Fieldglass** destination that was created when you run the booster to setup SAP Task Center.  
  ![Configure BTP Destinations 1](images/D1.png)
3. Edit the pre-created destination and update the properties below:  
   * __URL__: `https://<Your Fieldglass Tenant URL>/api/v1`
   * __Audience__: The Audience is used to construct the SAML assertion. For Example: `Fieldglass`.
   * __Client Key__: Add the `API Application Key` value located on the View Application Keys page in SAP Fieldglass Configuration Manager.
   * __Token Service URL__: `https://<Your Fieldglass Tenant URL>/api/oauth2/v2.0/token`
   * __Token Service User__: Add the `Virtual Person Name (Username)` value located in the Web Services section on the View Application Keys page in SAP Fieldglass Configuration Manager.
   * __Token Service Password__: Add the `License Key` value located in the Web Services section on the View Application Keys page in SAP Fieldglass Configuration Manager.
   * __Additional Properties__(To add an additional property, choose New Property and type in the property name and value.):
      * __tc.enabled__: `true`  (Make sure ‘t’ is lowercase in “tc.enabled”).
      * __tc.clientId__: This property is used to enable task updates to be pushed from SAP Fieldglass. The value of this property is the value of the `uaa > clientid` from the service key of the new service instance.
      * __tokenServiceURL.queries.client_id__: Add the `Client ID` value located on the View Application Keys page in SAP Fieldglass Configuration Manager.
      * __tokenServiceURL.queries.client_secret__: Add the `Client Secret` value located on the View Application Keys page in SAP Fieldglass Configuration Manager.
      * __URL.headers.X-ApplicationKey__: Add the `API Application Key` value located on the View Application Keys page in SAP Fieldglass Configu-ration Manager. This value is used when making calls to the URL in this destination.  
  ![Configure BTP Destinations 2](images/D2.png)
4. Select the **Use default JDK truststore** checkbox.  
5. Confirm that your setup looks similar to that in the screenshot and **save** your configuration.  

>**Note**  
>To check the connectivity between the SAP Task Center service and SAP Fieldglass, use the monitoring functionality of SAP Task Center. If you choose **Check Connection** in the destination configuration, you may not receive correct information about the connectivity between the SAP Task Center service and SAP Fieldglass.
