# Technical infrastructure documentation

## Key technical principles

Based on the technical principles described in [Technical principles](technical-principles.md), the SEM architecture is based on direct communication between parties with no central components. That implies that all parties will implement and publish a standard API. Which API is dependent on the ROLE the party plays.


# The big Picture

All parties have direct communication with each other. 
The parties that implement the API can be divided in 2 groups:
* parties that implement the API for their own business (like MP or LA)
* a SAAS vendor that implement the API for a school (like SIS and LMS)
 
SAAS Vendors will do the communication on behalf of a school after the school has given consent. They will not have an endpoint per school, but one endpoint as SAAS vendor.

![architecture](diagrams/Saas_Vendor_Infrastructure-Direct_Communication.drawio.svg)







## SEM Directory
So in total we will have a limitted list of parties in one region. 
The parties will know the other parties by the [SEM Directory](../SEM-Party-Directory.md)

##  Api authentication
For more information on authentication and authorization: See [API authentication](API-authentication.md)


# More detailed
![architecture](diagrams/Saas_Vendor_Infrastructure-Big_Picture_Gateways.drawio.svg)

# Detailed implementations
If a party plays multiple roles (like LA and MP), the party must implement multiple API's 


See [implementation Guides](implementation-guide.md)
