## Introduction

SAP Cloud Identity Services are needed for integrating task providers with SAP Task Center.

The SAP Cloud Identity Services comprise of the Identity Authentication (IAS) and Identity Provisioning (IPS).
Make sure that they are connected to your task provider (As explained in the next card: [Make sure that SAP Task Center and SAP Cloud Identity Services are connected](https://flpnwc-ad17b8dc3.dispatcher.hana.ondemand.com/sites/admincenter#projectboard-Display&/masterboard/4157/card/9301673).

Have a look at  

- SAP Cloud Identity Services - Identity Authentication [(link to the SAP Help documentation)](https://help.sap.com/viewer/p/IDENTITY_AUTHENTICATION)
- SAP Cloud Identity Services - Identity Provisioning [(link to the SAP Help documentation)](https://help.sap.com/viewer/product/IDENTITY_PROVISIONING/)
 
## Global User ID 

SAP Task Center requires a common unique identifier, the **Global User ID**, in your system landscape, for more details please have a look in the official documentation on the SAP Help Portal to get a detailed overview on how you can implement the **Global User ID**:

[Global User ID in Integration Scenarios](https://help.sap.com/docs/SAP_CLOUD_IDENTITY/b95c3d5bab324a3a8409eee5267a5b75/a04611df60404a248a7a8089c85b9761.html)

The recommended way is to use Identity Authentication which generates automatically the attribute, which is populated in the **User UUID** field or every newly created, imported or provisioned user.


For more information, see also: [Integrating the Service with SAP Task Center](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/ab5e90ebb2914be9aa145494df048a32.html).
