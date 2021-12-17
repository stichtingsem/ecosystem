# Technical infrastructure documentation

## Key technical principles

Based on the technical principles described in [Technical principles](technical-princples.md), the SEM architecture is based on direct communication between parties with no central components. That implies that all parties will implement and publish a standard API. Which API is dependent on the ROLE the party plays.


# The big Picture

All parties have direct communication with each other. 
The parties that implement the API can be dived in 2 groups:
* parties that implement the API for their own business (like MP or LA)
* a SAAS vendor that implement the API for a school (like SIS and LMS)
 
SAAS Vendors will do the communication on behalf of a school after the school has given consent. They will not have an endpoint per school, but one endpoint as SAAS vendor.

![architecture](diagrams/Saas_Vendor_Infrastructure-Direct_Communication.drawio.svg)







## SEM Directory
So in total we will have a limitted list of parties in one region. 
The parties will know the other parties by the [SEM Directory](../SEM-Party-Directory.md)

##  Api authentication
For more infoemation on authentication and authorization: See [API authentication](API-authentication.md)


# More detailed
![architecture](diagrams/Saas_Vendor_Infrastructure-Big_Picture_Gateways.drawio.svg)

# Detailed implementations
If a party plays multiple roles (like LA and MP), the party must implement multiple API's 


## SIS Gateway
The Learning Application will implement 1 API's and will send Events for these to other parties. As the SIS will not recieve events, the event hook api is not implemented

![architecture](diagrams/Saas_Vendor_Infrastructure-SIS_Vendor_Gateway.drawio.svg)

## MP Gateway
The Learning Application will implement 2 API's (entitlements and eventhooks) and will  recieve Events for these to other parties for Students, Usage and Catalogue.

![architecture](diagrams/Saas_Vendor_Infrastructure-MP_Gateway.drawio.svg)

## LMS Gateway
The LMS will implement no API's and will and will recieve Events from other parties for Students, Entitlements, Usage, Catalogue, Course 

![architecture](diagrams/Saas_Vendor_Infrastructure-LMS_Vendor_Gateway.drawio.svg)

## LA Gateway
The Learning Application will implement 4 API's and will send Events for these to other parties. It will send events for usage

![architecture](diagrams/Saas_Vendor_Infrastructure-LA_Gateway.drawio.svg)