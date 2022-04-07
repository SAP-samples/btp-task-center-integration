1. In your BTP subaccount, click **Destinations >> Download Trust**.  A file will be downloaded to your downloads folder.  This file is required when creating the communication system in S/4HANA Cloud.

![alt text](images/13-0.png)

2. Log into your S/4HANA Cloud system and access **Maintain Communication Users**.

![alt text](images/14.png)

3. Click **New** and create a new communication user.  Specify a **User Name, Description, and Password**.  Click **Create**.

![alt text](images/15.png)

4. Access **Communication Systems**.

![alt text](images/21.png)

5. Click New and specify a **System ID**, **System Name** and click **Create**.

![alt text](images/22.png)

6. Specify a value for **Host Name** to match your S/4Cloud hostname.  For eg. **myXXXXX.s4hana.ondemand.com**.

![alt text](images/23.png)

7. Enable OAuth 2.0 Identity Provider by setting the toggle to **ON**.

![alt text](images/25.png)

8. Click **Upload Signing Certificate** and upload the file your downloaded from the BTP subaccount in Step 1.

![alt text](images/26.png)

9. Copy the value after **CN=** and paste it in the **OAuth 2.0 SAML Issuer** text box.  Switch the **User ID Mapping Mode** to **User UUID**.

![alt text](images/24.png)

10. Click **+** under Users for Inbound Communication.

![alt text](images/27.png)

11. . Select the communication user created earlier and click **OK**.

![alt text](images/28.png)

13. Save your Communication System.
14. Access **Communication Arrangements**.

![alt text](images/16.png)

15. Click **New** and choose the value help icon to open up the list of available communication scenarios.

![alt text](images/17.png)

16. Search for **SAP_COM_0501** and select it. This communication scenario is relevant for Task Center integration.

![alt text](images/18.png)

17. Specify an **Arrangement Name** and click **Create**.

![alt text](images/19.png)

18. Use the value help icon and select the **Communication System** created earlier.  The User Name for inbound communication should automatically populate.  Confirm the Authentication Method is set to OAuth 2.0 and save your Communication Arrangement.

![alt text](images/29.png)

19. Click **OAuth 2.0 Detail** and make a note of the **Client ID**, **Token Service URL** and **SAML2 Audience**.  These fields are required to configure the destination settings in the BTP subaccount.

![alt text](images/30.png)
