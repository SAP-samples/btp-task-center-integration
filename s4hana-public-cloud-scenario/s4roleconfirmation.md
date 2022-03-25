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

