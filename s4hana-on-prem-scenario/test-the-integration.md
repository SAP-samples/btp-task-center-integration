Test your integration with the following steps:

1. Log on to SAP S/4HANA as an end user and use an application of your choice which creates tasks.   

2. Test if the task has arrived in SAP Task Center:  
    - Logon as the respective manager to SAP Task Center. In the SAP Launchpad service, choose the Task Center tile and search for the respective request. 
    - If you can't see the screen, you might have problems with missing permissions or user provisioning.   

3. Check if approval actions arrive back in SAP S/4HANA:
    - Approve a task in SAP Task Center, logon to the SAP S/4HANA system and see if the status of the business object, on which the task was based, has changed. As prerequisite, your tasks need to have arrived in SAP Task Center (see step 2). 
    - Logon to SAP Task Center as end user who has authorizations to approve the task you have created in step 1, choose the task in the overview list and press the *Approve* button. 
    - Logon to the SAP S/4HANA system using the user you used in step 1 and check if the status of your application has changed.