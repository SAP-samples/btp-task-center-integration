Test Task Center integration with the following steps.  
  
Log into SAP Fieldglass tenant as Hiring Manager and create an approval task. For example, you can create a job posting approval task in SAP Fieldglass.
1. Click on the **Create** button, and select **Job Posting for Worker** under **Contingent Labor**.  
  ![Test Integration 1](images/T1.png)
2. The Hiring Manager will select the Job Posting Template titled **Billing Analyst**.  
  ![Test Integration 2](images/T2.png)
3. Enter a Start Date. This should be a date at least 2 weeks into the past from today’s date. This is required, in order to submit timesheet(s), which is later in this
script. Then, enter an End Date, which can be +3-6 months from now.  
  ![Test Integration 3](images/T3.png)
4. Scroll Down to enter further details:
   * __Is travel required for position?__: `No`
   * __Legal Entity__: `1710`
   * __Site__: `Plant 1 US (1070)`
   * __Business Unit__: `Purch. Org 1710 (1710)`  
  ![Test Integration 4](images/T4.png)
5. Add a **Cost Center** and select **General Ledger Account**, click on **Submit** button.  
  ![Test Integration 5](images/T5.png)
6. Job Posting is created.  
  ![Test Integration 6](images/T6.png)
7. Login to **SAP Launchpad Service** with Approver user credentials.  
  ![Test Integration 7](images/T7.png)
8. Open **SAP Task Center**.  
  ![Test Integration 8](images/T8.png)
9. Click on **Task Center**.  
  ![Test Integration 9](images/T9.png)
10. Approve/Reject **Job Postings** in your Tasks.  
  ![Test Integration 10](images/T10.png)
11. Enter a Decision Note and Click on **Sumbit** button.  
  ![Test Integration 11](images/T11.png)
12. The task will disappear from the list, and return to SAP Fieldglass toconfirm that Job Posting is now in an approved status.  
  ![Test Integration 12](images/T12.png)
