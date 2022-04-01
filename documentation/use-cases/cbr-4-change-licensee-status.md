# CBR.4 Change Licensee Status

In this non-happy flow the Market Place wants to change the status of a single Licensee that activated the product of an Entitlement. The status can be changed from Activated to Blocked or vice versa.

![Process Diagram](../diagrams/process-diagrams-cbr-4-change-licensee-status.svg)

## Roles Involved

  - [Buyer](../roles/buyer.md)
  - [LMC](../roles/lmc.md)
  - [Sales Agent](../roles/sales-agent.md)
  - [Fulfilmment Agent](../roles/fulfilment-agent.md)
  
## Services Involved

  - [Learning Management System](../services/learning-management-system.md)
  - [Learning Application](../services/learning-application.md)
  - [Market Place](../services/marketplace.md)

## Basic Flow of Events

| No. | Input | Data | Process | Output |
|---|---|---|---|---|
| CBR.4.1 | N.A. | N.A. | MP sends a ChangeLicenseeEvent with the new status to the Learning Application and the Learning Management System. | ChangeLicenseeEvent Activated/Blocked. |
| CBR.4.2 | ChangeLicenseeEvent Activated/Blocked | N.A. | In case of a new status Blocked, the Learning Application blocks access to the Licensee. In case of a new status Activated, the Learning Application restores access for the Licensee. The Learning Application sends a ChangeLicenseeStatusConfirmation to the Market Place and updates the status of the Licensee to the new status. No Usage event is send with the new status. | ChangeLicenseeStatusConfirmation Activated/Blocked<br>All Licensees status changed to BLocked |
| CBR.4.3 | ChangeLicenseeEvent Activated/Blocked | Students<br>Product (Access URL)<br>Courses (Course URLs) | Learning Management System disables or enables all links the licensee. | ChangeLicenseeStatusConfirmation Blocked<br>Links disabled or enabled |
| CBR.4.4 | ChangeLicenseeStatusConfirmation Activated/Blocked (2x) | N.A. | Market Place receives ChangeLicenseeStatusConfirmations form both the Learning Application and the Learning Management System. After these confirmations the Market Place can take further actions regarding the Blocked or Activated Licensee. | Process Blocked or Activated Licensee in backoffice. |


## Preconditions

  - Digital fulfilment of Entitlement is completed.
  - Status of Entitlement is LinkReady or Cancelled

## Post-conditions

  - Learning Application prevents access to licensee (from activated to blocked) or restores access for the licensee (from blocked to activated)
  - Learning Application updated the status the licensee to the new status (No Usage Events are send for status changes of Licensees)
  - Learning Management System disabled (from activated to blocked) or eneabled (from blocked to activated) all links for Licensee