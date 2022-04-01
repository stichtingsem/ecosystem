# OA.3b Digital fulfilment of SchoolSubject Entitlements

In this process a SchoolSubject Entitlement is fulfilled to the [Users](../roles/user.md) related to the [Buyer](../roles/buyer.md) of the digital learning materials.

![Process Diagram](../diagrams/process-diagrams-oa-3b-digital-fulfilment-schoolsubject.svg)

## Roles Involved

  - [Fulfilmment Agent](../roles/fulfilment-agent.md)
  - [Learning Materials Provider](../roles/learning-materials-provider.md)
  - [Learning Management Provider](../roles/learning-management-provider.md)

## Services Involved

  - [Market Place](../services/marketplace.md)
  - [Learning Management System](../services/learning-management-system.md)
  - [Learning Application](../services/learning-application.md)

## Basic Flow of Events

| No. | Input | Data | Process | Output |
|---|---|---|---|---|
| OA.3b.1 | Entitlement SchoolSubject | N.A. | The Market Place in its role of Fulfilment agent triggers all digital fulfilment steps in sequence. | Send Entitlement to Learning Management System for adding of digital learning material to School Library<br>Send Entitlement to Learning Application for provisioning digital learning material for school<br>Send Provisioned Entitlement to Learning Management System for adding of product links to learning material lists of users |
| OA.3b.2 | Entitlement SchoolSubject | Product info from Catalogue<br> Course info from Course | The Learning Management System receives a new Entitlement from the Market Place. The digital learning material on this entitlement is added to the School Library of learning materials. This includes product links but also deeplinks to chapters and elements within the Course. | Digital Learning Material is available in the School Library<br>Course links are available in the School Library<br>All links are still disabled |
| OA.3b.3 | Entitlement SchoolSubject | N.A. | The Learning Application provisions the digital learning material for the school. A restriction is added that only students that follow one of the SchoolSubjects is allowed to activate the digital learning material | Digital learning material is provisioned for the School<br>An EntitlementConfirmation Provisioned is send to the Market Place |
| OA.3b.4 | EntitlementConfirmation Provisoned | N.A. | The Market Place receives an EntitlementConfirmation Provisioned from the Learning Application and changes the state of the Entitlement to Provisioned. | Entitlement state changed to Provisioned.<br>Learning Application and Learning Management System update the status change in their own backoffice systems. |
| OA.3b.5 | Entitlement SchoolSubject Provisioned | Students<br>SchoolSubjects<br> | The Learning Management System receives the status Provisioned for a SchoolSubject Entitlement from the Market Place. This allows the Learning Management System to automatically add the product links to the learning material lists of all Students that follow one of the SchoolSubjects. The links are automatically enabled after the start date. | Product links on the learning material lists of Students<br>The links are automatically enabled after start date<br>An EntitlementConfirmation LinkReady is send to the Market Place |
| OA.3b.6 | EntitlementConfirmation LinkReady | N.A. | The Market Place receives an EntitlementConfirmation LinkReady from the Learning Management System and changes the state of the Entitlement to LinkReady. | Entitlement state changed to LinkReady.<br>Learning Application and Learning Management System update the status change in their own backoffice systems. |

## Preconditions

  - The School ordered a digital learning material in OA.1 resulting into an Entitlement of the variant SchoolSubject.

## Post-conditions

  - Product and course links of the entitled digital learning material are added to the School Library with digital learning materials
  - Digital learning material is provisioned to the school
  - Product links are available on the learning material list of students


## Next process

The flow continues with the initial activation of the digital learning material by a User (OA.4).