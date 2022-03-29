1. Download the **SAML 2.0 metadata** file from the Administration Console of Identity Authentication service or using the URL https://<Identity_Authentication_tenant>.accounts.ondemand.com/saml2/metadata
![Enable SAP Task Center 1](images/S1.png)
2. Go to SAP Fieldglass and choose the **Configuration Manager** user.
![Enable SAP Task Center 2](images/S2.png)
3. Click on **View Single Sign-On** Tile.
![Enable SAP Task Center 3](images/S3.png)
4. On the Single Sign-On Setup page, choose **Edit**.
![Enable SAP Task Center 4](images/S4.png)
5. In the **Identity Provider Details** section, choose the **Upload** button to upload the client's metadata file using the **Identity Provider Metadata Import** tool.
![Enable SAP Task Center 5](images/S5.png)
![Enable SAP Task Center 6](images/S6.png)
6. In the **SAML Identity Location** property, choose **Attribute**, and in the **Attribute Name** text box, type sap_uid, Click **Next**.
![Enable SAP Task Center 7](images/S7.png)
7. In the **Service Provider Details** section, choose **Yes** for the **Enable Deep Linking In Notifications?** property, Click **Next**.
![Enable SAP Task Center 8](images/S8.png)
8. Click **Exit Wizard**.
![Enable SAP Task Center 9](images/S9.png)
