# Abstract
A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

## Functional and Technical documentation
The SEM Ecosystem is documented in a separate PDF file including functional and technical documentation. The [document](https://github.com/stichtingsem/ecosystem/blob/V1.3/docs/Documentatie%20SEM%20Ecosysteem.pdf) is a complete manual (in Dutch) for all parties that have interest in implementing one or more roles in the SEM Ecosystem. The document includes the following chapters:
1. Introduction: background information and design principles of the SEM Ecosystem.
2. Scenario's: description of the use cases supported by the SEM Ecosystem.
3. Functional documentation: description of domains, roles, definitions (including an Entity Relationship Diagram), interaction diagrams, transaction variants.
4. Architecture and security: explanation of the Event Driven Architecture that is used as a paradigm for the SEM Ecossytem and specification of the Security aspects including, OAuth, Token and scopes, and Consent.
5. Technical API documentation: The definition of all APIs and schemas. Within this chapter also rules can be found for filling of fields.
6. Appendix A: Scenario's for a closed money and goods flow (gesloten geld-goederenstroom)

## API reference Files
The API reference files are available on our [Public Github Repository](https://github.com/stichtingsem/ecosystem/reference). This Stoplight page is linked to the repository and is a representation of the reference files.

## API Documentation
The SEM Ecosystem is based on an Event Driven Architecture. This means that within the API documentation schemas are documented for all Events exchanged within a specific API. Most APIs also have GET endpoints to access single resources. More information can be found in the documentation, chapter 4 'Architecture and security'.

Each Party in the SEM Ecosystem provides and consumes APIs according to their roles. The table outlines these APIs.

| API Definition | Service Provider | Services Consuming | Remarks |
|---|---|---|---|
| [Events](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | all | all | All parties can send or recieve events |
| [Consent](https://stichtingsem.stoplight.io/docs/ecosystem/reference/consent.v1.yaml) | SIS, LA, MP | SIS: MP, LA, LMS<br>LA: LMS, SIS<br>MP: LMS | |
| [SIS](https://stichtingsem.stoplight.io/docs/ecosystem/reference/sisdata.v1.yaml) | SIS | MP, LA, LMS | |
| [Catalogue](https://stichtingsem.stoplight.io/docs/ecosystem/reference/catalogue.v1.yaml) | LA | MP, LMS | |
| [Course](https://stichtingsem.stoplight.io/docs/ecosystem/reference/coursee.v1.yaml) | LA | LMS | |
| [Entitlement](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | MP | LMS, LA | Entitlement communication requires a confirmation event reply from the LMS and LA |
| [Order](https://stichtingsem.stoplight.io/docs/ecosystem/reference/order.v1.yaml) | MP | LA | Order communication requires a confirmation event reply from the LA |
| [Usage](https://stichtingsem.stoplight.io/docs/ecosystem/reference/usage.v1.yaml) | LA | MP, LMS | |
| [Progress](https://stichtingsem.stoplight.io/docs/ecosystem/reference/progress.v1.yaml) | LA | LMS | First version with SimpleProgress |
| [Results](https://stichtingsem.stoplight.io/docs/ecosystem/reference/results.v1.yaml) | LA | LMS, SIS | First version with SimpleResult |

## Contact information
This repository is an initiative of the [Stichting Samenwerkende Educatieve Marktpartijen (SEM)](https://www.stichtingsem.org). For more information you can contact [Koen Voermans](mailto:koen.voermans@stichtingsem.org), Product Owner of SEM Ecosystem.
