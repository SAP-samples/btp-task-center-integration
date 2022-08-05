## Create Service User for Task Pull Service

Create a service user for granting access to the task pull service.


ℹ If you are running a co-deployed setup, with your front-end and back-end servers running on the same system, you create a service user on this single system.

1. Start transaction **SU01**.

2. Enter the name of the service user, and then choose **Create**.

3. On the **Logon Data** tab, select the user type **Service**, and enter a password.

4. On the Roles tab, add the role, which you have created with in the previouse step to this user.

> ⚠ Remember the user name and password to be used with your configuration of the destination on SAP Business Technology Platform.

ℹ The parth and settings might differ depending on your release version. Please check that you have selected the right version for [Create Service User for Task Pull Service](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/229c5a1f659341efa2bb6205159d6209.html?version=2021.002) in SAP Help documentation.

ℹ Screenhot from SAP S/4HANA 2020 FPS02 system.