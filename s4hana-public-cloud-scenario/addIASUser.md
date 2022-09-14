In order to access SAP S/4HANA Cloud users must also be created in SAP Cloud Identity Authentication tenant used with SAP S/4HANA Cloud.  In addition, users can be assigned to groups in SAP Cloud Identity Authentication that map to roles in SAP S/4HANA Cloud.  As you will see in the upcoming card, this setup allows us to provision users to SAP S/4HANA Cloud and assign them business roles using SAP Cloud Identity Provisioning service.

Procedure:

1. Access your Identity Authentication admin console.
2. Click **User Management** tile.

![alt text](images/iasusermanagement.png)

3. Click **+ Add User**.
4. Enter values for **FirstName**, **LastName**, **E-Mail**, **Login Name** fields and click **Save**. An account activation link will be sent to the user's email.

Note: These fields should match the user profile in S/4 HANA Cloud.  The login name(APPROVER) matches the username in SAP S/4HANA Cloud.

![alt text](images/iasadduser.png)

5. Activate the user account by following the link sent in the email.
6. Click **User Groups**.
7. Click **Create**.
8. Specify **Name**, **DisplayName**, and **Description** fields for the group and click **Create**.  The group name must match the role created in S/4HANA Cloud.  In our case this is called "PURCHASE_ORDER_APPROVER".

![alt text](images/iascreategroup.png)

9. Select the group you just created from the groups list.
10. Click **Add**, select the "Approver" user created earlier and click **Save**.
11. Confirm the user is added to the group.

![alt text](images/addusertogroup.png)

