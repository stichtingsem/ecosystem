# Abstract

A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

## Functional and Technical documentation

The SEM Ecosystem is documented in a separate PDF file including functional and technical documentation. The [document](https://github.com/stichtingsem/ecosystem/blob/master/docs/Documentatie%20SEM%20Ecosysteem.pdf) is a complete manual (in Dutch) for all parties that have interest in implementing one or more roles in the SEM Ecosystem. The document includes the following chapters:
1. **Introduction**: background information and design principles of the SEM Ecosystem.
2. **Scenario's**: description of the use cases supported by the SEM Ecosystem.
3. **Functional documentation**: description of domains, roles, definitions (including an Entity Relationship Diagram), interaction diagrams, transaction variants.
4. **Architecture and security**: explanation of the Event Driven Architecture that is used as a paradigm for the SEM Ecossytem and specification of the Security aspects including, OAuth, Token and scopes, and Consent.
5. **Technical API documentation**: The definition of all APIs and schemas. Within this chapter also rules can be found for filling of fields.
6. **Appendix A**: Scenario's for a closed money and goods flow (gesloten geld-goederenstroom)

## API Reference Files on [Github](https://github.com/stichtingsem/ecosystem)
The API reference files are available on our [Public Github Repository](https://github.com/stichtingsem/ecosystem) in the [reference folder](https://github.com/stichtingsem/ecosystem/tree/master/reference). This Stoplight page is linked to the repository and is a representation of the reference files.

## API Documentation

The SEM Ecosystem is based on an Event Driven Architecture. This means that within the API documentation schemas are documented for all Events exchanged within a specific API. Most APIs also have GET endpoints to access single resources. More information can be found in the documentation, chapter 4 'Architecture and security'.

Each Party in the SEM Ecosystem provides and consumes APIs according to their roles. The table outlines these APIs.

| API | Current version | Service Provider | Services Consuming | Remarks |
|---|---|---|---|---|
| [Events](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | 1.3.0 | all | all | All parties can send or recieve events |
| [Consent](https://stichtingsem.stoplight.io/docs/ecosystem/reference/consent.v1.yaml) | 1.3.0 | SIS, LA, MP | SIS: MP, LA, LMS<br>LA: LMS, SIS<br>MP: LMS | |
| [SIS](https://stichtingsem.stoplight.io/docs/ecosystem/reference/sisdata.v1.yaml) | 1.3.0 | SIS | MP, LA, LMS | |
| [Catalogue](https://stichtingsem.stoplight.io/docs/ecosystem/reference/catalogue.v1.yaml) | 1.3.0 | LA | MP, LMS | |
| [Course](https://stichtingsem.stoplight.io/docs/ecosystem/reference/coursee.v1.yaml) | 1.3.0 | LA | LMS | |
| [Entitlement](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | 1.3.0 | MP | LMS, LA | Entitlement communication requires a confirmation event reply from the LMS and LA |
| [Order](https://stichtingsem.stoplight.io/docs/ecosystem/reference/order.v1.yaml) | 1.3.0 | MP | LA | Order communication requires a confirmation event reply from the LA |
| [Usage](https://stichtingsem.stoplight.io/docs/ecosystem/reference/usage.v1.yaml) | 1.3.0 | LA | MP, LMS | |
| [Progress](https://stichtingsem.stoplight.io/docs/ecosystem/reference/progress.v1.yaml) | 1.3.0 | LA | LMS | First version with SimpleProgress |
| [Results](https://stichtingsem.stoplight.io/docs/ecosystem/reference/results.v1.yaml) | 1.3.0 | LA | LMS, SIS | First version with SimpleResult |

## Generic formatting rules and identifiers

For a couple of fields in the schema's generic formatting rules apply:

| Field | Type | Format | Rule | Example | Remark |
|---|---|---|---|---|---|
| Date | string | date | According to openapi, as specified in [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 'YYYY-MM-DD', 2017-07-21 | |
| Datetime | string | datetime | According to openapi in ZULU time, as specified in [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 2017-07-21T17:32:28Z | |
| createdAfter | string | datetime | According to openapi in ZULU time, as specified in [RFC 3339, section 5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 2017-07-21T17:32:28Z | In datetime format, applied in the GET Event(s) endpoints of the Events API |
| schemaVersion | string | string | According to the principles of [Semantic Versioning 2.0.0](https://semver.org) | 1.3.0 | |
| schoolId | string | digiDeliveryId | digiDeliveryId, case senstivie | 22461075-07B8-4A17-AB18-71B8455AA7A3 | Identifier of a the entity school, part of schema's. |
| schoolIdentifier | string | digiDeliveryId | digiDeliveryId, case senstivie | 22461075-07B8-4A17-AB18-71B8455AA7A3 | Identifier of a school, applied in the request for a token and also registration of consent. |
| eckId | string | ECK iD | ECK iD as generated by the Nummervoorziening and registered in the SIS. | https://ketenid.nl/pilot/7a73090b3ed60286fad2d1963c1bf610b3521027176cf38a23f3e1db12378e6ed74aac7b41e49be14fca764c8ddb495ac0076078b3b2bcfdcb1825d461e81960 | The ECK iD is used for Students and or Teachers. As an alternative the userId can be used, whenever the ECK iD is not known. The ECK iD requires strict handling, including: it shall not be stored in plain text in any of the systems (so also not in logging etc). |
| uuid | string | uuid | globally unique identifier | bd8e0494-168d-418f-8e01- 1a58d9effd54 | |


## Versioning

All APIs in the SEM Ecosystem have their own version number. This allows changes on an API level. The following rules apply to all parties who implement the APIs:
- Version numbers are based upon [Semantic Versioning 2.0.0](https://semver.org) principles.
- Every API has its own version number, all schema's within this API inherit this version number.
- All objects have a mandatory field `schemaVersion`, which refers to the version number of the schema.
- All GET endpoints have an optional query parameter `schemaVersion`, which enables a requestor to receive a response in a specified schemaVersion.
- In the Events API the endpoint `GET Schema Version for API` allows every party to request the supported schemaVersions of another party.
- All parties in the SEM Ecosystem support the previous version (t-1), and within reasonable time the current version (t). All older versions (t-2 or older) are not supported. This policy allows all parties to implement the current version within a reasonable time, but prevents the existence of many different versions of an API. If the change is business critical, it is possible to bypass this policy and request all parties to implement the new version.

## Contact information

This repository is an initiative of the [Stichting Samenwerkende Educatieve Marktpartijen (SEM)](https://www.stichtingsem.org). For more information you can contact [Koen Voermans](mailto:koen.voermans@stichtingsem.org), Product Owner of SEM Ecosystem.
