## Introduction

In this section, we need to grant access to a "admin" user who will maintain the SAP BTP launchpad site via the [Site Manager](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/Cloud/en-US/3f619a13ca2a4a59a14bec8507c3fb69.html).


## Adjust SAP BTP Laucnhpad role collection

The first step is now to modify the **Launchpad_Admin** role collection.
Please navigate to **Security > Role Collections** and select the **Launchpad_Admin** erntry:

![btp role](images/access_rc_lp_admin.png)

Select the role collection, switch in the edit mode and select the **User Groups** tab.
Click the **+** buton an enter in the **Name** a the group name (this needs to match with the group from Identiy Authentication), in this example *Admins* and save the changes:

![define rc group](images/lp_admin_role_collection_group.png)

* **Background: With this assigment it's possible to automatically assign users (which are staored in SAP Cloud Identity service) to the role collection.**
In the next step we will finalyze the configuartion on  SAP Cloud Identity services - Identiy Authentication.

## User creation on SAP Cloud Identity services - Identiy Authentication

Login to the SAP Cloud Identity services - Identiy Authentication tenant which is connected toh BTP Subaccount were SAP Task Center is running.
- Enter the **User Management** tile and create a user, example:

![user creation](images/lp_admin_user.png)

Now switch to **User Groups** and create a new group or like in this example to edit the **Admins** group an add the previously created user:

![modify group](images/assign_ias_lp_admin_2_group.png)

For more information about how to create a user, see [Create Users](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/a3bc7e863ac54c23ab856863b681c9f8.html).

## Validate the Identity Authentication setup

1. To validate the trust setup, execute SAP Launchpad service.
2. From the navigation menu, choose **Services > Instances and Subscriptions**.
3. To open the application, choose the **Go to Application** icon.

![open site manager](images/btp_open_lp_site_manager.png)

If you now log on with valid Identity Authentication credentials you should change the password: 

![open site manager](images/login_and_change_pw.png)

Afterwards you should now get access to the BTP Launchpad **Site Manager**:

![open site manager](images/btp_lp_site_manager.png)

## Result

With this we can now finsh the last step, where we integarte the SAP Taske Center applications, into a new launchpad site.