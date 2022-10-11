## Create Service User for Task Pull Service

Create a service user for granting access to the task pull service.


ℹ If you are running a co-deployed setup, with your front-end and back-end servers running on the same system, you create a service user on this single system.

1. Start transaction **SU01**.

2. Enter the name of the service user, and then choose **Create**.

3. On the **Logon Data** tab, select the user type **Service**, and enter a password.

    ![SU01 Service User](images/s4h-su01-create-service-user.png)

4. On the Roles tab, add the role, which you have created with in the previouse step to this user.

    ![SU01 Service User Role assignment](images/s4h-su01-service-user-role-assignment.png)


> ⚠ Remember the user name and password to be used with your configuration of the destination on SAP Business Technology Platform.


ℹ The path and settings might differ depending on your SAP S/4HANA release version. Please check that you have selected the right version for [Create Service User for Task Pull Service](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/229c5a1f659341efa2bb6205159d6209.html?version=2021.002) in the SAP Help Portal documentation.

ℹ Screenshot from SAP S/4HANA 2020 FPS02 system.

