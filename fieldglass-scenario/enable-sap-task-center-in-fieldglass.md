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
6. In the **SAML Identity Location** property, choose **Attribute**, and in the **Attribute Name** text box, type sap_uid, click **Next**.  
![Enable SAP Task Center 7](images/S7.png)
7. In the **Service Provider Details** section, choose **Yes** for the **Enable Deep Linking In Notifications?** property, click **Next**.  
![Enable SAP Task Center 8](images/S8.png)
8. The **Finished** step opens, confirming you have finished SSO setup, click **Exit Wizard**.  
![Enable SAP Task Center 9](images/S9.png)
9. Click on **Actions -> Download SP Metadata**.  
![Enable SAP Task Center 10](images/S10.png)
10. Go to your Identity Authentication Service Admin Console. Create a new application under **Applications**.   
![Enable SAP Task Center 11](images/S11.png)
11. Enter a **Name** of your Fieldglass tenant, and choose **SAP Fieldglass solution** as the type of your application.  
![Enable SAP Task Center 12](images/S12.png)
12. Click on **SAML 2.0 Configuration**.
![Enable SAP Task Center 13](images/S13.png)
13. Click on **Browse** to upload the Fieldglass metadata. 
![Enable SAP Task Center 14](images/S14.png)
14. **Save** the configuration.  
![Enable SAP Task Center 15](images/S15.png)
15. Click on **Subject Name Identifier**.  
![Enable SAP Task Center 16](images/S16.png)
16. Select **User UUID** as a basic attribute and **Save**.
![Enable SAP Task Center 17](images/S17.png)
17. Click on **Assertion Attributes**.
![Enable SAP Task Center 18](images/S18.png)
18. Add/Modify **User UUID** mapping to **sap_uid** and **Save**.
![Enable SAP Task Center 19](images/S19.png)
19. Contact SAP Fieldglass Customer Support at https://www.fieldglass.com/customer-support. Information published on non-SAP site to request assistance with enabling the custom script sso.sapid2uname for the company. 

