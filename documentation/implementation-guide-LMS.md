# Implementation Guide LMS

##TLDR

The LMS needs/should to implement the folowing:
* register with SEM
* retrieve list of all available SIS, MP and LA's in your region
* Setup with alls SIS, MP and LA parties that you do business with.
* Implement API endpoints
  * Events api endpoint
  * Consent flow API 
  * Entitlement API (for the LMS endpoints)
* Create a UI for a school administrator to 
  * give consent to receive data from a SIS
  * give consent to receive data from a MP
  * give consent to reciev data from several LA's
* Receive events about school students and teachers
* Retrieve product information from each LA's catalogue and subscribe to updates
* recieve events about product updates
* recieve entitlements from the MP 
  * show links for students
  * retrieve course information from LA for used products
* receive events about progress from the LA's and display

# TODO : more details


## LMS Gateway
The LMS will implement 3 API's and will and will recieve Events from other parties for Students, Entitlements, Usage, Catalogue, Course 

![architecture](diagrams/Saas_Vendor_Infrastructure-LMS_Vendor_Gateway.drawio.svg)
