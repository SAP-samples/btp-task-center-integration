After enabling SAP Task Center in SAP Fieldglass, follow this procedure to establish trust with the SAP Destination service.

##Procedure

1. To export your trust certificate in the SAP BTP cockpit where your SAP Task Center instance was created, navigate to your Cloud Foundry subaccount and then select Connectivity Destinations from the navigation area on the left.
Select Download Trust.
 
**Note**
Make sure to renew your trust certificate before it expires. For the time while you are renewing the trust certificate and updating it for SAP Fieldglass, you may not be able to work on tasks, nor receive task updates. For more information, see Renew Destination Trust Certificates.
 
2. Save the trust certificate file locally with extension .cer.
3. Contact your SAP Fieldglass representative to upload this certificate in the SAP Fieldglass tenant Truststore.

**Limitations**

SAP Fieldglass currently only supports these limited modules for the SAP Task Center service:
* Job Posting
* Work Order
* Work Order Revision
* Statement of Work (SOW)
* Project
* Profile Worker
