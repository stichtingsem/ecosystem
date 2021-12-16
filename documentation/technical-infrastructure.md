# Technical infrastructure documentation

## Key technical principles


A simple overview of a generic exchange is as follows, note that while this may look complex at first glance, it is a common pattern used in the B2B software space and is straight forward to implement on both sides of the exchange:

# The big Picture
All parties have direct communication with each other

![architecture](diagrams\Saas_Vendor_Infrastructure-Direct_Communication.drawio.svg)

## How many parties do we expect in a region

| Type | # |
-------------|---------
Marketplaces| just a few
LMS vendors | 3 or 4
SIS vendors | 2 or 3
LA Learning applications| around 10 ?

So in total we will have a limitted list of parties in one region


## More detailed
![architecture](diagrams\Saas_Vendor_Infrastructure-Big_Picture_Gateways.drawio.svg)

# Detailed implementations
## SIS Gateway
The Learning Application will implement 1 API's and will send Events for these to other parties. As the SIS will not recieve events, the event hook api is not implemented

![architecture](diagrams\Saas_Vendor_Infrastructure-SIS_Vendor_Gateway.drawio.svg)

## MP Gateway
The Learning Application will implement 2 API's (entitlements and eventhooks) and will  recieve Events for these to other parties for Students, Usage and Catalogue.

![architecture](diagrams\Saas_Vendor_Infrastructure-MP_Gateway.drawio.svg)

## LMS Gateway
The LMS will implement no API's and will and will recieve Events from other parties for Students, Entitlements, Usage, Catalogue, Course 

![architecture](diagrams\Saas_Vendor_Infrastructure-LMS_Vendor_Gateway.drawio.svg)

## LA Gateway
The Learning Application will implement 4 API's and will send Events for these to other parties. It will send events for usage

![architecture](diagrams\Saas_Vendor_Infrastructure-LA_Gateway.drawio.svg)