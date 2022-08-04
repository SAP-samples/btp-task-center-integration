# Connect SAP S/4HANA and SAP Task Center

1. Configure and enable the communication between your SAP S/4HANA system (ABAP system) and SAP Task Center. Thefore some configuration steps need to be done in your SAP S/4HANA system. In the **Implementation Guide**, choose *SAP Customizing Implementation Guide > ABAP Platform  Application Server  Business Management > SAP Business Technology Platform > Integration  SAP Task Center Integration.<sup>i</sup>*  
![SAP S/4HANA IMG config](images/s4h-img-tree.png)

2. In the BTP subaccount where SAP Task Center is enabled, configure a destination used for task retrival for the SAP S/4HANA sytem. 

**Check** the prerequisits section of [Connect SAP S/4HANA and SAP Task Center
](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/143af9bb452f4aa5a9980035d9edee5b.html)

>⚠ **Caution** For the set up of SAP Task Center, you must have a Cloud Connector that uses user UUID as the subject pattern for principal propagation.

<sup>i</sup> The parth and settings might differ depending on your release version. Please check that you have selected the right version for [Configuring SAP Task Center Integration](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/5117f21ef28f4e698d99fe3fdbc1be2a.html?version=2021.002) in SAP Help documentation.