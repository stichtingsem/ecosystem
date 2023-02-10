# SEM Ecosytem

## Note: Legal status of the specifications in this repository
 > All information in this repository is in concept. No rigths can be claimed based on this information.

## Abstract

A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

## Structure of this repository

This repository consists of the following elements:
- [Functional and technical documentation](https://github.com/stichtingsem/ecosystem/blob/master/docs/Documentatie%20SEM%20Ecosysteem.pdf) is described within a PDF file.
- [API files](https://github.com/stichtingsem/ecosystem/tree/master/reference) can be found in the Github repository in the reference folder.
- [API documentation](https://stichtingsem.stoplight.io/docs/ecosystem) can be found on stoplight.

This repository is an initiative of the Stichting Samenwerkende Educatieve Marktpartijen (SEM).

## Moving from a chain to an ecosystem

Stichting Samenwerkende Educatieve Marktpartijen (SEM) is a foundation where private parties work together. Within a large group of organizations there exists the wish to simply the way all parties work together in order to deliver (digital) learning materials to the end-users within Dutch schools. This was the reason to start an investigation both on CEO as on CTO level how this can be achieved. The investigation resulted in the design of a new technical standard: the SEM ecosystem.

The SEM ecosystem tries to overcome the main challenges in the current learning materials chain (leermiddelenketen in Dutch):
- The current chain is build upon principles of the supply of physical learning materials. Moreover, administrative processes are leading. This leads to issues in the immediate access to digital learning materials.
- There is a large dependency between parties within the current chain. On the other hand is the use of standards and the commitment to industry agreements open-ended. Parties are therefore able to (not) use these standards and agreements without obligation.
- The current chain is too complex for the end-users within schools.
- The technology used within the current chain is end-of-life.

The SEM ecosystem has the following benefits for schools and market parties:
- Flexiblity in the selection of learning materials for schools.
- Possibility to offer new business models for market parties.
- Transparency in transactions and usage information for both schools and market parties.
- Aggregated insight into progress information and results for teachers and students.
- Schools are in control of the data that is exchanged between market parties (consent).

## Join the SEM Foundation and adopt the SEM Ecosystem standard

All organisations offering products and/or services to Dutch schools are welcome to join the SEM Foundation and adopt the SEM Ecosystem.

## Version history

| Version | Date | Status | Author | Comment |
|---|---|---|---|---|
| 0.1 | 2 December 2021 | DRAFT | [@kvoer](https://github.com/kvoer) | |
| 0.2 | 7 December 2021 | DRAFT | [@kvoer](https://github.com/kvoer) | |
| 1.1 | 15 February 2022 | REJECTED | [@kvoer](https://github.com/kvoer) | Change of Entitlement API to synchronous exchange mechanism not approved |
| 1.1 | 1 April 2022 | Approved | [@kvoer](https://github.com/kvoer) | Entitlement API redefined based on Events Driven Architecture<br>For the PoC in Q2, Entitlements based on POST endpoints |
| 1.2 | 22 April 2022 | Approved | [@kvoer](https://github.com/kvoer) | Non-happy flows and regulations for mutations approved in steering committee. |
| 1.2 | 26 April 2022 | Approved | [@mcginkel](https://github.com/mcginkel) | catalogue: is now status mandatory |
| 1.2 | 29 April 2022 | Approved | [@jorimvdw](https://github.com/jorimvdw) | consent API: doc update, requestsync now with api parameter iso consumerrefid |
| 1.2.0 | 25 May 2022 | Approved | [@kvoer](https://github.com/kvoer) | Simple Result API added |
| 1.3.0 | 3 February 2023 | Approved | [@kvoer](https://github.com/kvoer) | All issues from PoC2 resolved and documentation written |

## Contributors

This standard is developed by members from [Stichting SEM](www.stichtingsem.org). The contributors to the SEM Ecosystem standard are:

| Name | Organization | Role | Alias |
|---|---|---|---|
| Clifton Cunningham | Infinitas Learning | Initiator | [@cliftonc](https://github.com/cliftonc) |
| Koen Voermans | Stichting SEM | Product Owner | [@kvoer](https://github.com/kvoer) |
| Marcel Untied | Stichting SEM | Project Leader poc phase 1 | [@MarcelUntied](https://github.com/orgs/stichtingsem/people/MarcelUntied) |
| Edwin Verwoerd | Iddink Group | Member working committee | [@edwinverwoerd](https://github.com/edwinverwoerd) |
| Henk Haarsma | Noordhoff Uitgevers | Member working committee | [@hhaarsma](https://github.com/hhaarsma) |
| Jan van der Wel | Topicus Education | Member working committee | [@mrVanderWel](https://github.com/mrVanderWel) |
| Sanne Visseren | Malmberg | Member working committee | |
| Bart van Kimmenade | It's Learning | Member review group | [@bvankimmenade](https://github.com/bvankimmenade) |
| Danny Pronk | The Learning Network | Member review group | [@dpronk](https://github.com/dpronk) |
| Frank van der Bom | Malmberg | Member review group |  |
| Jerry Plate | Iddink Group | Member review group |  |
| Jolanda Brittijn | Malmberg | Member review group |  |
| Jorim van den Wijngaard | Topicus Education | Member review group | [@jorimvdw](https://github.com/jorimvdw) |
| Linse Goeman | Malmberg | Member review group |  |
| Peter Veenstra | Osingadejong | Member review group | [@PeterVeenstraOdj](https://github.com/PeterVeenstraOdJ) |
| Roy Eysbach | ThiemeMeulenhoff | Member review group |  |
| Tamara Koster | Noordhoff Uitgevers | Member review group | [@tamarakoster](https://github.com/tamarakoster) |
| Elias Hassing | Infinitas Learning | Lead Functional Track poc phase 2 | [@eliashassing154](https://github.com/eliashassing154) |
| Frank Aarts | ThiemeMeulenhoff | Member Technical Track PoC phase 2 | [@TM-Frank](https://github.com/orgs/stichtingsem/people/TM-Frank) |
| Kees van Ginkel | Iddink Group | Member Technical Track Poc phase 2 | [@mcginkel](https://github.com/mcginkel) |
| Luke Niesink | Topicus Education | Member Technical Track PoC phase 2 | [@niesink](https://github.com/niesink) |
| Sieger Kuik | Stichting SEM | Lead Administrative Track PoC phase 2 | [@SiegerKuik](https://github.com/siegerkuik) |
