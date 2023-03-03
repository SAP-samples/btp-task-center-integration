## Create a secondary SAP Cloud for Customer destination for the principal propagation

**Step 1: Principal Propagation Flow and Set Up**

**Configure SAP Business Technology Platform as OAuth Identity Provider in Cloud for Customer**

1.	In the SAP Business Technology Platform cockpit, choose your **Global Account** and your subaccount name from the **Subaccount** menu in the breadcrumbs.

2.	Navigate to **Connectivity > Destinations**.

3.	Select **Download Trust** to download the primary signing certificate of the subaccount.

![Download-Trust](images/donwload-trust.jpg)

4.	Open the downloaded file in a text editor, copy the certificate content (everything between —–BEGIN CERTIFICATE—– and —–END CERTIFICATE—–) to a new file, and save the new file.

5. In SAP Cloud for Customer, navigate to **Administrator > Common Tasks > Configure OAuth 2.0 Identity Provider**.

![Configure-OAuth2](images/new-oauth-provider.jpg)

6. Select **New OAuth 2.0 Provider**.

7.	Enter a name in the **Issuing Entity Name** field in this format: **cfapps.<region_host>/(subaccountID)**
  
8.	Browse and upload the primary signing certificate.

9.	Enable **Email Address** in addition to **User Account ID** under **Select Name ID Formats**.

10.	Click **Submit**.
  
![Issuing Entity](images/oauth-provider-new.jpg)


