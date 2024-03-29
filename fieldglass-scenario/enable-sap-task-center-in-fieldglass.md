1. Download the **SAML 2.0 metadata** file from the Administration Console of Identity Authentication service or use the URL `https://<Identity_Authentication_tenant>.accounts.ondemand.com/saml2/metadata`.  
  ![Enable SAP Task Center 1](images/S1.png)
2. Go to SAP Fieldglass and choose the **Configuration Manager** user.  
  ![Enable SAP Task Center 2](images/S2.png)
3. Choose the **View Single Sign-On** tile.  
  ![Enable SAP Task Center 3](images/S3.png)
4. On the **Single Sign-On** Setup page, choose **Edit**.  
  ![Enable SAP Task Center 4](images/S4.png)
5. In the **Identity Provider Details** section, choose the **Upload** button to upload the client's metadata file using the **Identity Provider Metadata Import** tool.  
  ![Enable SAP Task Center 5](images/S5.png)
![Enable SAP Task Center 6](images/S6.png)
6. Choose **Attribute** as the **SAML Identity Location**, in the **Attribute Name** text box, type `sap_uid`, and choose **Next**.  
  ![Enable SAP Task Center 7](images/S7.png)
7. In the **Service Provider Details** section, choose **Yes** for the **Enable Deep Linking In Notifications?** property, and choose **Next**.  
  ![Enable SAP Task Center 8](images/S8.png)
8. The **Finished** step opens, confirming you have finished the SSO setup, and choose **Exit Wizard**.  
  ![Enable SAP Task Center 9](images/S9.png)
9. Choose **Actions -> Download SP Metadata**.  
  ![Enable SAP Task Center 10](images/S10.png)
10. Go to your Identity Authentication Service Admin Console. Create a new application under **Applications**.   
  ![Enable SAP Task Center 11](images/S11.png)
11. Enter the **name** of your SAP Fieldglass tenant and choose **SAP Fieldglass solution** as the type of your application.  
  ![Enable SAP Task Center 12](images/S12.png)
12. Choose **SAML 2.0 Configuration**.  
  ![Enable SAP Task Center 13](images/S13.png)
13. Choose **Browse** to upload SAP Fieldglass metadata.  
  ![Enable SAP Task Center 14](images/S14.png)
14. **Save** the configuration.  
  ![Enable SAP Task Center 15](images/S15.png)
15. Choose **Subject Name Identifier**.  
  ![Enable SAP Task Center 16](images/S16.png)
16. Select **User UUID** as a basic attribute and **save**.  
  ![Enable SAP Task Center 17](images/S17.png)
17. Choose **Assertion Attributes**.  
  ![Enable SAP Task Center 18](images/S18.png)
18. Modify the **User UUID** mapping to be **sap_uid** and **save**.  
  ![Enable SAP Task Center 19](images/S19.png)
19. Contact SAP Fieldglass Customer Support at [https://www.fieldglass.com/customer-support](https://www.fieldglass.com/customer-support) to request assistance with enabling the custom script `sso.sapid2uname` for the company. 

