## Test Task Center integration with the following steps.  
  
1. Log into your SAP Fieldglass tenant as Hiring Manager and create an approval task. For example, you can create a job posting approval task in SAP Fieldglass.
2. Click on the **Create** button and select **Job Posting for Worker** under **Contingent Labor**.  
  ![Test Integration 1](images/T1.png)
3. The Hiring Manager will select the Job Posting Template titled **Billing Analyst**.  
  ![Test Integration 2](images/T2.png)
4. Enter a **start date**. This should be a date at least 2 weeks into the past from today’s date. This is required, to submit timesheet(s), which is later in this
script. Then, enter an **end date**, which can be +3-6 months from now.  
  ![Test Integration 3](images/T3.png)
5. Scroll down to enter further details:
   * __Is travel required for position?__: `No`
   * __Legal Entity__: `1710`
   * __Site__: `Plant 1 US (1070)`
   * __Business Unit__: `Purch. Org 1710 (1710)`  
  ![Test Integration 4](images/T4.png)
6. Add a **cost center** and select **General Ledger Account**, Choose **Submit**.  
  ![Test Integration 5](images/T5.png)
7. The job posting is created.  
  ![Test Integration 6](images/T6.png)
8. Log into **SAP Build Work Zone** with Approver user credentials.  
  ![Test Integration 7](images/T7.png)
9. Open **SAP Task Center**.  
  ![Test Integration 8](images/T8.png)
10. Choose **Task Center**.  
  ![Test Integration 9](images/T9.png)
11. Approve or reject the **Job Postings** in your task list.  
  ![Test Integration 10](images/T10.png)
12. Enter a decision note and choose **Sumbit**.  
  ![Test Integration 11](images/T11.png)
13. The task will disappear from the list and return to SAP Fieldglass to confirm that Job Posting is now approved.  
  ![Test Integration 12](images/T12.png)
