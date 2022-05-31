# Technical reference documentation

## Key technical principles

The SEM implementation is based on these 9 Technical principles. See : [principles](technical-principles.md)

## Architecture

The architecture of the SEM implementation is described in [Technical Architecture](technical-infrastructure.md)





## Webhooks and events

TODO: Explain the architectural model and the usage of webhooks and events.

A simple overview of a generic exchange is as follows, note that while this may look complex at first glance, it is a common pattern used in the B2B software space and is straight forward to implement on both sides of the exchange:

![architecture](diagrams/event-architecture.svg)

## Security by design using open standards

The security and data minimization approach is outlined here: [security](https://github.com/stichtingsem/technology-prototype/issues/18)

TODO: Finalize the discussion and describe the definite security aspects in this paragraph

## Other relevant standards

TODO: Describe all relevant standards for parties that want to join the ecosystem.

## Information model

TODO: What is the underlying information model used within the ecosystem?

## APIs

Each Party in the SEM Ecosystem provides and consumes APIs according to their roles. The table outlines these APIs.

| API Definition | Service Provider | Services Consuming | Remarks |
|---|---|---|---|
| [Events](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | all | all | All parties can send or receive events |
| [Webhooks](https://stichtingsem.stoplight.io/docs/ecosystem/reference/events.v1.yaml) | all | all | |
| [Consent](https://stichtingsem.stoplight.io/docs/ecosystem/reference/consent.v1.yaml) | SIS, LA, MP | SIS: MP, LA, LMS<br>LA: LMS, SIS<br>MP: LMS | |
| [SIS Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/sisdata.v1.yaml) | SIS | MP, LA, LMS | |
| [Catalogue Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/catalogue.v1.yaml) | LA | MP, LMS | |
| [Course Data](https://stichtingsem.stoplight.io/docs/ecosystem/reference/coursee.v1.yaml) | LA | LMS | |
| [Receive Entitlements](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | LA, LMS | MP | The LA and LMS receive entitlements from the MP. This is transactional. |
| [Entitlements](https://stichtingsem.stoplight.io/docs/ecosystem/reference/entitlement.v1.yaml) | MP | LMS, LA | Entitlements can be checked at the MP, First activation |
| [Usage](https://stichtingsem.stoplight.io/docs/ecosystem/reference/usage.v1.yaml) | LA | MP, LMS | |
| [Progress](https://stichtingsem.stoplight.io/docs/ecosystem/reference/progress.v1.yaml) | LA | LMS | To be defined |
| Results | LA | LMS, SIS | To be defined |
