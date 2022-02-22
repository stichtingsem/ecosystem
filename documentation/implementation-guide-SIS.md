# Implementation Guide SIS

##TLDR

The SIS needs/should to implement the folowing:
* register with SEM
* retrieve list of all available LMS, MP and LA's in your region
* Setup with alls LMS, MP and LA parties that you do business with.
* Implement API endpoints
  * Events api client to send events
  * Webhook API to recieve webhooks from LMS, MP and LA's
  * Consent flow API 
* Create a UI for a school administrator to
  * display consent request from LA,MP,LMS
  * give consent to send events data to a LMS
  * give consent to send events to a MP
  * give consent to send events to several LA's
* after consent and webhook registration: Send one event per teacher and one per student to the other party
* Send events about updates on students and teachers. (incl changes in Subjects and groups)


# TODO : more details

## SIS Gateway
The SIS Application will implement 2 API's and will send Events for these to other parties. As the SIS will not recieve events, the event hook api is not implemented

![architecture](diagrams/Saas_Vendor_Infrastructure-SIS_Vendor_Gateway.drawio.svg)
