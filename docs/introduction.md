# Abstract
A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

All information is available on our [Public Github Repository](https://github.com/stichtingsem/ecosystem/). This repository is an initiative of the Stichting Samenwerkende Educatieve Marktpartijen (SEM) and is based upon the [principles](https://github.com/stichtingsem/ecosystem/principles.md) defined in the working document [Moving from a chain to an ecosystem](https://github.com/stichtingsem/ecosystem/documentation/documents/).

## API Specification

Each Party in the SEM Ecosystem provides and consumes APIs according to their roles. The table outlines these APIs.

| API Definition | Service Provider | Services Consuming | Remarks |
|---|---|---|---|
| [Events](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | all | all | All parties can send or recieve events |
| [Webhooks](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | all | all | |
| [Consent](https://stichtingsem.stoplight.io/docs/ecosystem/reference/consent.v1.yaml) | SIS, LA, MP | SIS: MP, LA, LMS<br>LA: LMS, SIS<br>MP: LMS | |
| [SIS Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/sisdata.v1.yaml) | SIS | MP, LA, LMS | |
| [Catalogue Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/catalogue.v1.yaml) | LA | MP, LMS | |
| [Course Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/coursee.v1.yaml) | LA | LMS | |
| [Recieve Entitlements](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | LA, LMS | MP | The LA and LMS recieve entitlements from the MP. This is transactional. |
| [Entitlements](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | MP | LMS, LA | Entitlements can be checked at the MP, First activation |
| [Usage](https://stichtingsem.stoplight.io/docs/ecosystem/reference/usage.v1.yaml) | LA | MP, LMS | |
| [Progress](https://stichtingsem.stoplight.io/docs/ecosystem/reference/progress.v1.yaml) | LA | LMS | To be defined |
| Results | LA | LMS, SIS | To be defined |

## Further reading
- [Big Picture](https://github.com/stichtingsem/ecosystem/big-picture.md) which explains all the concepts within the ecosystem in more detail.
- [Technical reference](https://github.com/stichtingsem/ecosystem/technical-reference.md) with information about the architecture, used standards and links to the reference files.
- [Implementation Guide](https://github.com/stichtingsem/ecosystem/documentation/implementation-guide.md) with practical advice for new parties.
- [Glossary](https://github.com/stichtingsem/ecosystem/glossary.md) describing all terms and definitions used within the ecosystem.
- [SEM Party directory](https://github.com/stichtingsem/ecosystem/SEM-Party-Directory.md) with all Parties that are currently active in the ecosystem.

