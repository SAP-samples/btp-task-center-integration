## Create Communication Arrangement C4C

1.	Navigate to **Administrator > General Settings > Integration > Communication Arrangements**.

![Communication_Arrangements](images/Communication-Arrangements.png)

2.	Select **New** to create a new communication arrangement.

3.	Select **Rest Services** as the communication scenario and click **Next**.

![Communication_Scenario](images/admin-create-comm-arrange.jpg)

4.	Under **Communication System**, enter the **System Instance ID** of the communication system with which you want to set up communication arrangements and click **Next**.

![Communication_Arrangement](images/Communication-arrangement.png)

5.	In the next step, select the communication scenarios for which you want to create the communication arrangements. 
Under **Inbound Communication: Basic Settings:** Check the details on the **Inbound tab** as necessary:

Enabled: If you do not want to use a service, uncheck the checkbox. If the service is mandatory, the checkbox is disabled.

Application Protocol: Check if the protocol is Web Service.

Select the **Authentication Method** – UserID and Password. 
In the **User ID** field, click **Edit Credentials**.

The user ID of the communication user is created automatically. Provide a **password** and select **SAP Task Center Provider Service**.

![Communication_Arr_Services_Used](images/Comm-scenario-services-used.png)

Note down the **user ID**, the provided **password**, and the **URL** of your SAP Cloud for Customer tenant . These details are then required while creating primary destination with the technical user.

6.	Click on **next** and review all the configuration details:

![Communication_Arrangement_Review](images/comm-arrange-review.jpg)

7.	In the next screen, A success message is shown once the communication arrangement has been created successfully.

![Communication_Arrangement_Confirmation](images/Comm_Arr_Confirmation.png)


