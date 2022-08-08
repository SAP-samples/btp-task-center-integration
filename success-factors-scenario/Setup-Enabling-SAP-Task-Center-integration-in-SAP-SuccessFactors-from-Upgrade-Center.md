Follow these steps to enable SAP Task Center in SAP SuccessFactors by adding permissions and using the SAP SuccessFactors Upgrade Center:

Step 1: Assign role-based permission to admin user performing configuration in SAP SuccessFactors:

Logon to the SAP SuccessFactors system and go to **Admin Center-> Manage Permission Roles**.
Choose the permission category **Administrator Permissions ->Manage User**.
select the following checkboxes:
**Read Access to SCIM User API**
**Edit Access to SCIM User API**
Go to **Administrator Permissions-> Manage Integration Tools**  and select **Access to Integration Service Registration Center UI** check box.
Step 2: Enable To-Do Task Integration between SAP SuccessFactors and SAP Task Center using the Upgrade Center:

Logon to the SAP SuccessFactors system and go to **Admin Center ->Upgrade Center**.
Find the **Enhanced To-Do Integration upgrade** and choose **Learn More & Upgrade Now**. This step provides important background information about the upgrade. Choose **Upgrade Now**.
**NOTE**: If you don't find Enhanced To-Do Integration on the landing page of the Upgrade Center, check under View Saved for Later Items.

With this step, the records of the past 3 months of the SAP SuccessFactors categories affected by the integration are prepared for the initial load into SAP Task Center.

You can find list of supported tasks here: -[Supported Tasks for Enhanced To-Do Integration - SAP Help Portal](https://help.sap.com/docs/PRODUCT_ID/568480cc877d4337992a2cd9792fbfed/cbb89cf9d70e4dafb005338f5ab93c3c.html?state=PRODUCTION&version=latest&locale=en-US)
