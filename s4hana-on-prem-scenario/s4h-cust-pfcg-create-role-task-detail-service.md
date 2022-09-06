## Create Role for Task Detail Service

Create an authorization role on your back-end system for granting access to the task detail service.

1. Start transaction **PFCG** and enter the name of the role (according to your naming conventions). Then choose **Role > Create Single Role** .

2. On the **Menu** tab, choose **Authorization Default** from the **Insert Node** menu.

3. In the **Authorization Default** field on the **Service** popup, select **SAP Gateway OData V4 Backend Service Groups & Assignments**.

4. In the **TADIR Service** field, select the **(G4BA) API_TASK_SPI_DETAILS** service using the value help.

5. Choose **Apply**, then **Copy**.

6. The Role Menu contains the added entry.

7. On the **Authorizations** tab, choose **Expert Mode for Profile Generation**.

8. If the **Group/Object/Authorization/Field** column, Object **Class BC_A > Authorization Object S_SCOPE** shows a yellow status for values missing.
    - Right-click Authorization Object **S_SCOPE** and choose **Deactivate**.

9. **Save** and **generate** the role.


<sup>i</sup> The path and settings might differ depending on your release version. Please check that you have selected the right version for [Create Role for Task Detail Service](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/fef6f08bd6f248f6a0c9d643b281709d.html?version=2021.002) in SAP Help Portal documentation.