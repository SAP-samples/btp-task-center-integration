# Scenario Overview


SAP Task Center on SAP Business Technology Platform integrates with SAP S/4HANA.

For SAP S/4HANA as task provider all approval use cases are supported as approvals are enabled by the underlying workflow engine by default. Thus all (standard + custom) approvals can be processed via the SAP Task Center service on SAP BTP. See also [Supported Solutions and Use Cases](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/758209c5763840b3bce63327a02debbb.html) and [FAQs on SAP community page for SAP Task Center ](https://community.sap.com/topics/task-center/faq)
## Prerequisites
Before enabling the integration scenario between SAP S/4HANA and SAP Task Center Service:

* Please check [SAP Note "2975987 - ABAP Platform Integration with SAP Task Center"](https://launchpad.support.sap.com/#/notes/2975987) to be sure that your current SAP S/4HANA version is supported as task provider for SAP Task Center.

* Please check also on corrections under component "BC-BMT-WFM" which might be applied to the scenario and your SAP S/4HANA version. See also [SAP Note "3044195 - SAP Task Center Support Components"](https://launchpad.support.sap.com/#/notes/3044195)

* Please check that the administrator setting up the integration to SAP Task Center must have the permissions in SAP S/4HANA to perform the configuration steps mention here: [Configuring SAP Task Center Integration](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/0f18dddf28764f5b807ecd80549044cc/5117f21ef28f4e698d99fe3fdbc1be2a.html?version=latest)
### Connect SAP S/4HANA and SAP Task Center

In general this mission is based on the SAP Help Portal documentation [Connect SAP S/4HANA and SAP Task Center](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/143af9bb452f4aa5a9980035d9edee5b.html) and [Connect SAP S/4HANA Cloud, Private Edition and SAP Task Center](https://help.sap.com/docs/TASK_CENTER/08cbda59b4954e93abb2ec85f1db399d/50ce13335bb4404cb0eddebb37de0855.html?version=Cloud)

**! Please pay attention to always select the version applicable to your SAP S/4HANA system in the SAP Help Portal documentation!**

![SAP Help - Version selection](images/s4h_sap-help-business-workflow_sap-help_version_selection.png)
