# Consent flow

__Introduction__
    
One of the core principals of SEM is that the school should be in charge of deciding who can access their data. The data is therefor only shared when a person with certain rights (for example: a privacy officer) has given consent to share data with 2 parties in de ecosystem. For example: a privacy officer gives consent in the SIS to share data with an MP, and gives consent in the MP to receive the SIS-data. Once the consent is given in both systems, the actual data is shared.

![consent](documentation/diagrams/consentbasic.svg)

The school must give consent for the following data exchanges:
- SIS to MP, LMS & LA (SIS-data)
- LA to LMS (Usage, Progress & Results)
- MP to LMS (Entitlements)

To streamline this process we developed the consent-api. The core principal is when consent is given (or revoked), the other party is notified of this change. For this purpose an optional callbackurl is registered alongside the client. For example: if consent is revoked in the SIS to share data with a MP, the MP recieves notification that this happened.

Scenarios:

SIS to MP, LM & LA:

The consent process can be started in either the SIS or the MP, LM or LA. When consent is given in the SIS, a consent request is sended to the other party. The received request needs to be made visible in the other system. A person with certain rights (in some cases the same person as in the SIS) needs to approve or decline this consent:

![consent](documentation/diagrams/consentflowsis.svg)

This process can also be turned around. Then the process starts in the MP, LM or LA. Important is that in all cases the consent is given on both sides:

![consent](documentation/diagrams/consentflowsisreversed.svg)

The same goes for the exchange of usage, progress & results from the LA to a LMS, and for the sharing of entitlements from the MP. Consent can be started in either system, but consent needs to be given in both systems before data is shared. 

The user can also revoke a prior given consent. An updatemessage will than also be send to the callbackurl. At all times a party can check the status of the consent in the other system. Status can be Active or Revoked.

![consent](documentation/diagrams/consentflowextra.svg)
