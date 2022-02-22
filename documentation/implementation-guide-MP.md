# Implementation Guide MP

##TLDR

The MP needs/should to implement the folowing:
* register with SEM
* retrieve list of all available SIS, LMS and LA's in your region
* Setup with alls SIS, LMS and LA parties that you do business with.
* Implement API endpoints
  * Events api endpoint
  * Webhook client to register with SIS and LA's
  * Consent flow API
  * Entitlement API (for the MP endpoints)
* Create a UI for a school administrator to 
  * give consent to receive data from a SIS
  * give consent to send data to a LMS
  * give consent to recieve/send data from several LA's
* Receive events about school students and teachers
* Retrieve product information from each LA's catalogue and subscribe to updates
* recieve events about product updates
* create something to create entitlements for a school
* send the entitlements to the LA's
* when the entitlements to the LMS'
* recieve first activation requests from LA
* receive events about usage from the LA's

* implement process of changing entitlements, sending updates to LA's and LMS

* Implement UX to show school admin the overview and usage of entitlements/licenses

# TODO : more details

## MP Gateway
The Learning Application will implement 3 API's (entitlements, entitlements and events) and will  recieve Events for these to other parties for Students, Usage and Catalogue.

![architecture](diagrams/Saas_Vendor_Infrastructure-MP_Gateway.drawio.svg)