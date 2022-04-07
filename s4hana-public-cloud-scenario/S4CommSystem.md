1. In your BTP subaccount, click **Destinations >> Download Trust**.  A file will be downloaded to your downloads folder.  This file is required when creating the communication system in S/4HANA Cloud.
<img alt="BTP Trust set up2" src="images/2.png" />

2. Log into your S/4HANA Cloud system and access **Maintain Communication Users**.
<img alt="BTP Trust set up14" src="images/14.png" />

3. Click **New** and create a new communication user.  Specify a **User Name, Description, and Password**.  Click **Create**.
<img alt="BTP Trust set up15" src="images/15.png" />

4. Access **Communication Systems**.
<img alt="BTP Trust set up21" src="images/21.png" />

5. Click New and specify a **System ID**, **System Name** and click **Create**.
<img alt="BTP Trust set up22" src="images/22.png" />

6. Specify a value for **Host Name** to match your S/4Cloud hostname.  For eg. **myXXXXX.s4hana.ondemand.com**.
<img alt="BTP Trust set up23" src="images/23.png" />

7. Enable OAuth 2.0 Identity Provider by setting the toggle to **ON**.
<img alt="BTP Trust set up25" src="images/25.png" />

8. Click **Upload Signing Certificate** and upload the file your downloaded from the BTP subaccount in Step 1.
<img alt="BTP Trust set up26" src="images/26.png" />

9. Copy the value after **CN=** and paste it in the **OAuth 2.0 SAML Issuer** text box.  Switch the **User ID Mapping Mode** to **User UUID**.
<img alt="BTP Trust set up24" src="images/24.png" />

10. Click **+** under Users for Inbound Communication.
<img alt="BTP Trust set up25" src="images/27.png" />

11. . Select the communication user created earlier and click **OK**.
<img alt="BTP Trust set up28" src="images/28.png" />

13. Save your Communication System.
14. Access **Communication Arrangements**.
<img alt="BTP Trust set up16" src="images/16.png" />

15. Click **New** and choose the value help icon to open up the list of available communication scenarios.
<img alt="BTP Trust set up17" src="images/17.png" />

16. Search for **SAP_COM_0501** and select it. This communication scenario is relevant for Task Center integration.
<img alt="BTP Trust set up18" src="images/18.png" />

17. Specify an **Arrangement Name** and click **Create**.
<img alt="BTP Trust set up19" src="images/19.png" />

18. Use the value help icon and select the **Communication System** created earlier.  The User Name for inbound communication should automatically populate.  Confirm the Authentication Method is set to OAuth 2.0 and save your Communication Arrangement.
<img alt="BTP Trust set up29" src="images/29.png" />

19. Click **OAuth 2.0 Detail** and make a note of the **Client ID**, **Token Service URL** and **SAML2 Audience**.  These fields are required to configure the destination settings in the BTP subaccount.
<img alt="BTP Trust set up30" src="images/30.png" />
