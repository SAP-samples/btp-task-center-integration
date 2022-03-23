1. Access your BTP Subaccount. Under **Destinations**, select **S4HANACloud** destination that is created when you run the booster to setup Task Center.
<img src="31.png"/>
2. Edit the pre-created destination and update the properties below:
  - **URL**: <Your S/4HANA Cloud API URL> eg: https://myXXXXX-api.s4hana.ondemand.com
  - **Audience**: <Paste the SAML2 Audience value captured from OAuth 2.0 details in S/4)
  - **Token Service URL**: <Paste the Token Service URL value captured from OAuth 2.0 details in S/4>
  - **Client Key**: <Paste the Client ID value captured from OAuth 2.0 details in S/4>
  - **Token Service User**: <Communication user created in S/4HANA Cloud earlier>
  - **Token Service Password**: <Password for the Communication User>
  - **Additional Properties**:
    * __URL.queries.sap-client__: 100
    * __tc.enabled__: true  //Click New Property and type property name and value.  Make sure ‘t’ is lowercase in “tc.enabled”.
3. Confirm that your setup looks similar to the one in the screenshot. **Save** your configuration.
<img src="32.png"/>
