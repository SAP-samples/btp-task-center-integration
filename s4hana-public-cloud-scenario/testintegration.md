Test your integration with the following steps.

1. Log on to SAP S/4HANA Cloud system and create an approval task. For example, you can create a purchase order approval task. 
2. Test if the task has arrived in SAP Task Center:
* Logon as the respective manager to SAP Task Center. In the Launchpad, choose the Task Center tile and search for the leave request. 
* If you can't see the screen, you might have problems with missing permissions or user provisioning.
* As an alternative, to see if the task arrived, you can log on to SAP Task Center as an administrator and choose the administrator tile Task Center Administration in the Launchpad. Therein you will see how many tasks arrived. 
    If it's not enough for you to see how many tasks arrived and you want to see if the task arrived correctly, you can download the tasks using an API for data download from SAP Task Center cache. This is explained in detail in this blog. 
     Check if approval actions arrive back in SAP SuccessFactors: Approve a task in SAP Task Center, logon to the SAP SuccessFactors system and see if the status of the business object, on which the task was based, has changed. As prerequisite, your tasks need to have arrived in SAP Task Center (see step 2). The following procedure illustrates with the example of a leave request:
3. Logon to SAP Task Center as person who can approve tasks, choose the purchase approval taks created above and press the approve button. 
