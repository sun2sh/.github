<table>
<tr>
<td>

# ONDC - Open Network for Digital Commerce

ONDC is an ambitious initiative to democratize digital commerce by creating a decentralized network of buyer apps and seller apps through an interoperable protocol specification.

## Overview

This comprehensive guide is designed to walk you through the process of integrating your digital commerce platform with the Open Network for Digital Commerce (ONDC). By following these steps, you'll enable seamless interoperability with the decentralized network, allowing your platform to leverage the benefits of ONDC.

## Table of Contents

1. [Getting Started](#getting-started)
2. [Quick Start Guide](#quick-start-guide)
3. [The Protocol](#the-protocol)
4. [Subscription Process](#subscription-process)
5. [Signing and Verification](#signing-and-verification)
6. [Enabled Domains](#enabled-domains)
7. [Reference Applications](#reference-applications)
8. [Utilities](#utilities)

## Getting Started

[NP Profile Form](https://docs.google.com/forms/d/e/1FAIpQLScKKSuBUg2FbKaQjAiaYoptA2OVig01oNNNSYv5mzqTrxAbCA/viewform) is a registration form for all entities that wish to integrate with ONDC. Filling the NP Profile Form is necessary for starting your integration with ONDC.

## Quick Start Guide

[ONDC Integration Guide](https://docs.google.com/presentation/d/1HPRXk3lVYKmyAFcApgukZuwHhIZ_VlqR/edit#slide=id.g27b2e3e34a2_28_199) is a roadmap designed to illuminate key resources and navigate through the integration journey.

## The Protocol

**Beckn** is an open protocol that allows local businesses across any industry to be discovered and engaged by any beckn-enabled application. **Beckn protocol** is a collection of open specifications consisting of protocol APIs, message formats, network design and reference architectures to allow any two entities to execute commercial transactions without being on the same platform.

**ONDC** has provided the network extension layer over the Beckn Protocol (base layer),together it comprises the **ONDC protocol**. Over the base layer, the network extension layer comprises **model specifications** customised to the ONDC context that have been adopted in order to facilitate transactions over the network.

### Subscription Process

To enroll in the ONDC network, Network Participants (NP) must be added to the registry. The steps for an NP to onboard onto the ONDC Registry (Staging, Pre Production, Production) are outlined as follows:

1. **Staging Registry**

   - Obtain whitelisting for the subscriber ID.
   - Initiate the subscription process by calling the /subscribe API.
     The complete process is documented [here](https://github.com/ONDC-Official/developer-docs/blob/main/registry/Onboarding%20of%20Participants.md)
2. **Pre-Production Registry**

   After presenting a demo and receiving approval from the relevant team, follow the [outlined process](https://github.com/ONDC-Official/developer-docs/blob/main/registry/Onboarding%20of%20Participants.md) to be added to the Pre-Prod registry. 
3. **Production Registry**
   Upon successfully completing functional testing and satisfying the final checklist in Pre-Production, an NP can transition to the the Production environment.

### Signing and Verification

When communicating over HTTP using Beckn APIs, the subscribers need to authenticate themselves to perform transactions with other subscribers. Due to the commercial nature of the transactions, every request/callback pair is considered to be a "contract" between two parties. Therefore, it is imperative that all requests and callbacks are digitally signed by the sender and subsequently verified by the receiver.

The complete process is documented [here](https://github.com/ONDC-Official/developer-docs/blob/main/registry/signing-verification.md)

### Enabled Domains

Below are links to the comprehensive developer guide and model implementations for the enabled domains.

- Retail - This domain encompasses subcategories such as grocery, food and beverages, fashion, electronics, home & decor, beauty, and personal care, etc. It facilitates seamless transactions in both B2C and B2B modes, offering a comprehensive shopping experience for consumers and businesses alike.

  - B2C

    - [v1.2](https://docs.google.com/document/d/1brvcltG_DagZ3kGr1ZZQk4hG4tze3zvcxmGV4NMTzr8/edit)
    - [Test Case Scenarios - B2C](https://docs.google.com/spreadsheets/d/1JZV6ZQzXcHUsOwegGtArX3DdIXYIy3gxkhQ00q7kICc/edit#gid=1367601795)
  - B2B

    - [v2.0.2](https://github.com/ONDC-Official/ONDC-RET-Specifications/tree/release-2.0.2)
    - [Test Case Scenarios - B2B](https://docs.google.com/document/d/10ouiTKLY4dm1KnXCuhFwK38cYd9_aDQ30bklkqnPRkM/edit)
  - [Retail Developer Guide](https://ondc-official.github.io/ONDC-RET-Specifications/)

     - `For B2B, select version : release-2.0.2`
     - `For B2C, select version : draft-1.x`

- Logistics - This domain streamlines the acquisition of on-network logistics services, providing logistics buyers with a variety of choices for flexible solutions that suit their specific needs.

  - [v1.2](https://docs.google.com/document/d/1CkfxtqyLbSQccJZyNmf9BSGzJBH13gcLOk_tywV-LBk/edit)
  - [B2B Logistics](https://github.com/ONDC-Official/ONDC-LOG-Specifications)
  - [Logistics Developer Guide](https://ondc-official.github.io/ONDC-LOG-Specifications/)
       - `For B2B Logistics, select version : draft-2.x`
  - [Test Case Scenarios - Logistics](https://docs.google.com/spreadsheets/d/1JZV6ZQzXcHUsOwegGtArX3DdIXYIy3gxkhQ00q7kICc/edit#gid=1670900093)
- Financial Services - This domain facilitates easy access to a spectrum of financial solutions, covering loans, insurance, investments. 

  - [Financial Services Developer Guide](https://ondc-official.github.io/ONDC-FIS-Specifications/)

       - `For Loan , select Version : draft-loan`
       - `For Insurance , select version : draft-insurance`
       - `For Investments , select version : draft-mutual-funds`

  - [Gift Card](https://docs.google.com/document/d/1iTCQd_jI3mRqgSiaeZBvxWL-G_wkE__xxW-Wua8arVE/edit)

  - [Test Case Scenarios](https://docs.google.com/spreadsheets/d/1JZV6ZQzXcHUsOwegGtArX3DdIXYIy3gxkhQ00q7kICc/edit#gid=1670900093)

- Travel & Tourism - This domain enables easy access to a range of travel-related services, covering On-demand Ride hailing with various transport modes, ticket booking without designated seat. 

  - [Mobility Specifications Developer Guide](https://ondc-official.github.io/mobility-specification/)

      - `For On-demand Ride hailing, select version : draft-TRV10-2.0.0`
      - `For Unreserved Ticket Booking, select version : draft-TRV11-2.0.0`


- Services -  This domain empowers individuals to effortlessly access a diverse array of services, covering home services like painting and consulations, etc.

  - [v2.0.0](https://github.com/ONDC-Official/ONDC-SRV-Specifications/tree/draft-services)
  - [Services Developer Guide](https://ondc-official.github.io/ONDC-SRV-Specifications/#)

- Ancillary Services

  - Issue & Grievance Management (IGM) within the ONDC Network serves as a critical mechanism for resolving disputes and concerns among Network Participants (NPs).
    - [v1.0.0](https://docs.google.com/document/d/1UYGIo1fSOcA4ypnk5FuaCgUgNnu9dBQt/edit)
  - Reconcillation and Settlement Framework (RSF) plays a pivotal role in maintaining a comprehensive trail of settlements between Network Participants.
    - [v1.0.0](https://docs.google.com/document/d/1ubUPAWpbbUJ4vG2h5TQ74srZBjYjrO0P/edit)
  - Rating 
    - [v1.2.0](https://docs.google.com/document/d/1VaafY8t47hjpoW6tdezGsPwLwxxaAaGc/edit)
  - Score
    - [v1.2.0](https://docs.google.com/document/d/126O1wFdA-IuwojiAuLzdpN36vjWfQg9KOA2zRd9-zTY/edit#heading=h.bifjra7hj5b0)
  - [Test Case Scenarios (IGM &amp; RSF)](https://docs.google.com/document/d/1tx86sypacIRXgL9nlNBdvHz7cYQjQoyC/edit)

## Reference Applications

The network participants need to complete the end-to-end testing with ONDC reference applications.

**Staging Environment**

- [ONDC Reference Seller App](https://ref-app-seller-staging-v2.ondc.org/sign-up)
  - Github Repo [link](https://github.com/ONDC-Official/seller-app-sdk/tree/master)
- [ONDC Reference Buyer App](https://ref-app-buyer-staging-v2.ondc.org/login)
  - Github Repo [link](https://github.com/ONDC-Official/ondc-sdk)
- [ONDC Reference LSP App](https://ref-logistics-app-stage.ondc.org/)
  - Github Repo [link](https://github.com/ONDC-Official/ref-logistics-app-sdk/tree/main)

**Pre-Production Environment**

- [ONDC Reference Seller App](https://seller-app-preprod-v2.ondc.org/sign-up)
  - Github Repo [link](https://github.com/ONDC-Official/seller-app-sdk/tree/master)
- [ONDC Reference Buyer App](https://buyer-app-preprod-v2.ondc.org/login)
  - Github Repo [link](https://github.com/ONDC-Official/ondc-sdk)
- [ONDC Reference LSP App](https://ref-logistics-app-preprod.ondc.org/)
  - Github Repo [link](https://github.com/ONDC-Official/ref-logistics-app-sdk/tree/main)

## Utilities

- Signing and Verification : This tool is designed to support and aid ONDC Network Participants in constructing their own cryptocurrency libraries essential for engaging with the ONDC Network. It encompasses tasks such as key generation, signing, verification, encryption, and decryption.
  - [Java](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/ondc-crypto-utility-master)
  - [NodeJS](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/ondc-crypto-sdk-nodejs)
  - [Python](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/signing_and_verification)
  - [GoLang](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/signing_and_verification/golang)
- [Subcription process](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/on_subscibe-service) : This tool aids ONDC Network Participants during the subscription process for the registry (Staging, Pre Prod, Prod). It includes the implementation of the /on_subscribe API in both NodeJS and Python.
- [Retail/IGM Log Verification](https://github.com/ONDC-Official/log-validation-utility) : This tool is designed for ONDC Network Participants to verify their transaction logs related to the Retail and IGM use cases on their end, ensuring accuracy before submission to the ONDC team for technical clearance.
- [B2B/Logistics Log Verification](https://github.com/ONDC-Official/reference-implementations/tree/main/utilities/logistics-b2b/log-verification-utility) : This tool is designed for ONDC Network Participants to verify their transaction logs related to the B2B and Logistics use cases on their end, ensuring accuracy before submission to the ONDC team for technical clearance.
- [vlookup](https://www.npmjs.com/package/vlookup-ondc) : This tool is developed to perform a registry lookup and retrieve details related to Network Participants (NP).

</td>
<td width="30%"  style="vertical-align: top;"><img src="profile/ONDC-Logo.png"></td>
</tr>
</table>
