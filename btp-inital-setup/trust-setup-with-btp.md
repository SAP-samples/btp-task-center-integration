#Introduction

SAP Task Center supports the user universal unique identifier (UUID) to ensure the identification of the end user in each connected system, for example, SAP S/4HANA with a unique identifier.

To support this, you are required to use the user universal unique identifier(UUID) of the [Identity Authentication service](https://help.sap.com/products/IDENTITY_AUTHENTICATION?version=Cloud) as the federation identifier.

For more information, see Identity Lifecycle: SAP Reference Architecture for Identity Access Management – Part 2.

##Configuration

To enable trust in your subaccount on SAP BTP, see also [Establish Trust and Federation Between UAA and Identity Authentication](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/161f8f0cfac64c4fa2d973bc5f08a894.html).

Choose one of the following options:

- [Automatic trust setup](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/b9f4b0dc967040c99c7c8268ce335cce.html?q=establish%20trust) (described below)
- [Manual trust setup](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/36214a93a8864662996a0d0814f3e1b7.html?q=establish%20trust%3Fq%3Destablish%20trust)

##Automatic trust setup

In your subaccount, you can establish automatic trust that is set up with the following steps:

1. From the navigation menu, choose Security > Trust Configuration.

<img src="pics/establish_trust_cockpit.png" width="300">
