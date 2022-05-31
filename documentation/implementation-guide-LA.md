# Implementation Guide LA

##TLDR

The LA needs/should to implement the folowing:
* register with SEM
* retrieve list of all available SIS, MP and LMS's in your region
* Setup with all SIS, MP and LA parties that you do business with.
* Implement API endpoints
  * Events api endpoint
  * Webhook client to register with SIS
  * Consent flow API 
  * Usage API
  * Catalogue API
  * Progress API
  * Results API
  * Entitlement API (for the LA endpoints)
* Create a UI for a school administrator to 
  * give consent to receive data from a SIS
  * give consent to receive data from a MP
  * give consent to send progress data  to the LMS
* Initial sync of Catalogue with MP and LMS and Course with LMS
  * [S.2 Setup of Market Place for a new Learning Application (Catalogue)](documentation/use-cases/s.1.0-learning-application-sales-agent.md)
  * [S.3 Setup of Learning Management System for a new Learning Application (Catalogue and Course)]
* Receive events about school students and teachers
* send events about product updates to all parties that have registered a webhook and have given consent
* receive entitlements from the MP
* allow students to access your methods
  * if this is the first time a student uses your product: send activation to MP
* send usage information events to MP
* send progress events to LMS
* respond to change entitlement requests from the MP



# TODO : Add more details

## LA Gateway
The Learning Application will implement 5 API's and will send Events for these to other parties. It will send events for usage, catalogue, course, progress

![architecture](diagrams/Saas_Vendor_Infrastructure-LA_Gateway.drawio.svg)