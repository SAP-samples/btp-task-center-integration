
# Creating Approval Tasks in SAP C4C - Opportunity Approval

**Pre-requisites**

1. **Scope-in Multi-Step Approval for Opportunities in Business Configuration**

    * Login with **UserID**.
    * Go to **Business Configuration** → **Implementation Projects**. Select the project **First Implementation** and click on **Edit Project Scope**.
    * In the guided activity page, click on **Next** twice to reach the step 3 - **Review Questions**.
    * On the left navigation tree for **Scoping Element**, select **Sales** → **New Business** → **Opportunities**.
    * Select **'In Scope'** for the question **'Do you want to use a multiple step approval process for opportunities...'** and then click on **Next**.
    
      ![Review-Questions](cloud-for-customer/Complete-project-setup.png)
      
    * Add a **Title** and **Description** (optional) and click on **Finish**.


2. **Enable Submit for Approval for Custom Status**

    * Login with **purchasing_manager** or **administrator**.
    * Go to **Business Configuration** → **Overview**.
    * Search for  Activity **'Opportunities'** and click on it to open it.
    * In the displayed factsheet click on link **'Maintain Custom Status'**.
    * Select the document type **OPPT** in the header table **'Available Document Types'**.
    * For Life Cycle Status entry **'2 - In process'**, select the checkbox **'Submit for Approval'**.
    * **Save**.


3. **Define Approval Process**

    * Login with your **UserID**.
    * From **Administrator** → **Approval Processes**, define an approval Process for Opportunity with either **'Reporting Line Manager'** or **'Direct Approver'** as work distribution. Here as an example, we setup a process where any Opportunity with Name starting with the string **'TaskCenter'** must be sent to approval to Tim Lebel (purchasing_manager)
    * Screenshot 


**Task Creation and Approval**

1. **Create a Task**

    * Login with **purchaser**.
    * From **Sales → Opportunities**, Create a new Opportunity by entering the following details:
    **Name**: Any string starting with **TaskCenter**
    **Account**: Enter **1000010 (University Hospital)**.
    * On click of **Save** a new approval task will be created for the **purchasing_manager** who is the reporting line manager of **purchaser**. 
    * Screenshot: 
    * The current approver can be confirmed by opening the Opportunity detail screen and navigating to the tab **Approval**.


2. **Approving the task**

    * Login with **purchasing_manager**
    * Click on the Bell icon on the top right of shell to see all notifications with recently assigned approval task coming on top.
    * Click on **Approve** icon to approve the task.
