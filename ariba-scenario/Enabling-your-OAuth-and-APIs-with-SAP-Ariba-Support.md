Contact SAP Ariba Technical Support and work with them to help enable your API and IDP Registration for SAP Ariba OAuth. There will need to be a few technical enablement tasks done by SAP Ariba Support to get this enabled. This is needed to allow the security configurations to allow the seamless flow of user and task information between SAP Ariba and SAP Task Center.

On the SAP Ariba Developer Portal create an application for each SAP Ariba product you want to use (SAP Ariba Buying, SAP Ariba Sourcing, or create two applications if you want to use both). Contact SAP Ariba Technical Support and provide the application key, realm name and share the SAP Ariba product it needs to link to. Follow these steps:

 a. Create an application on the SAP Ariba Developer Portal for each SAP Ariba product you would like to connect to SAP Task Center. For more information about accessing the SAP Ariba Developer Portal, see [Help for the SAP Ariba developer portal](https://help.sap.com/docs/ARIBA_APIS/b61dd8c7e22c4fe489f191f66b4c48d6/1d55722e669e4c6aaa4eda5a011519ac.html).

 b. Save the application key for each created application.

 c. Once your applications are created, locate the URL for the application. Format example is - https://openapi.ariba.com/api/procurement-task-provider/v2/prod
 
The Token Service URL is the same for both SAP Ariba Buying and SAP Ariba Sourcing. Example for US data center - https://api.ariba.com/v2/oauth/token

 d. To request the activation of the application on the SAP Ariba Developer Portal, provide the following information to SAP Ariba Technical Support:
   - The Application key of the application, created on the SAP Ariba Developer Portal
   - The product that the request is for (SAP Ariba Buying or SAP Ariba Sourcing)
   - Realm name
   - The data center where your SAP Ariba realm resides

 e. To request IDP registration on the SAP Ariba OAuth, provide the following information to SAP Ariba Technical Support:
   - Your SAP Ariba realm name or customer site name (see Prerequisites)
   - Entity Identifier (entityID) in the SAML assertion request
     The entityID is sent by the destination service and must be in the following format:
     cfapps.${S1_LANDSCAPE_DOMAIN}/${S1_SUBACCOUNT_ID}.
     For example, cfapps.sap.hana.ondemand.com/abcd1234-ab12-ab12-ab12-abcd1234abcd1234.
     For more information, see [User Propagation between Cloud Foundry Applications](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/8ebf60c82a8e4cfc904f441c0c0acd6b.html?locale=en-US).
   - The destination service certificate
     To get the destination service certificate, log on to your Cloud Foundry subaccount, select the Destinations tab from the navigation area on the left, and choose Download Trust to download the destination service certificate.

     Caution
     Make sure to renew you trust certificate before it expires. For the time while you are renewing the trust certificate and updating it on the task provider systems you may not be able to work on tasks, nor receive task updates.
     For more information, see [Renew Destination Trust Certificates](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/8080abf7d2cf4918802aa86e955ffc8b.html#renew-destination-trust-certificates).

   - Your Ariba Network ID (ANID or NetworkId)
     You can find it in your Company Profile. For more information, see [SAP Ariba Glossary](https://help.sap.com/docs/SAP_Ariba/19025eff298741f78ecfff03d35e9331/a784eae0f6864284959945a77caef3dc.html?locale=en-US) and [How to specify your company profile information](https://help.sap.com/docs/ARIBA_NETWORK/5c0bdb0caa3042a288b3a1fb83b2fb1e/dd7e8953f0181014846b9461fdc68461.html?locale=en-US).
