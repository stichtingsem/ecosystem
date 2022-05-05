# SEM Ecosytem Standard

## Note: Legal status of the specifications in this repository
 > All information in this repository is draft. No rigths can be claimed based on this information
 > The standards can change without notice until they are finalised and approved

## Abstract

A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

## Structure of this repository

This repository consists of the following elements:
- [Big Picture](big-picture.md) which explains all the concepts within the ecosystem in more detail.
- [Technical reference](documentation/technical-reference.md) with information about the architecture, used standards and links to the reference files.
- [API documentation](https://stichtingsem.stoplight.io/docs/ecosystem) can be found on stoplight.
- [Implementation Guide](documentation/implementation-guide.md) with practical advice for new parties.
- [Glossary](glossary.md) describing all terms and definitions used within the ecosystem.
- [SEM Party directory](SEM-Party-Directory.md) with all Parties that are currently active in the ecosystem.

This repository is an initiative of the Stichting Samenwerkende Educatieve Marktpartijen (SEM) and is based upon the [principles](documentation/principles.md) defined in the working document [Moving from a chain to an ecosystem](documentation/documents/).

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

All organisations offering products and/or services to Dutch schools are welcome to join the SEM Foundation and adopt the SEM Ecosystem. The  [SEM Party Directory](SEM-Party-Directory.md) lists all Parties that are currently active in the Ecosystem.

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

## Contributors

This standard is developed by members from [Stichting SEM](www.stichtingsem.org). The contributors to the SEM Ecosystem standard are:

| Name | Organization | Role | Alias |
|---|---|---|---|
| Clifton Cunningham | Infinitas Learning | Initiator | [@cliftonc](https://github.com/cliftonc) |
| Danny Pronk | The Learning Network | Member Technical Track | [@dpronk](https://github.com/dpronk) |
| Elias Hassing | Infinitas Learning | Lead Functional Track | [@eliashassing154](https://github.com/eliashassing154) |
| Edwin Verwoerd | Iddink Group | Member Technical & Administrative Track | [@edwinverwoerd](https://github.com/edwinverwoerd) |
| Frank Aarts | ThiemeMeulenhoff | Member Technical Track | [@TM-Frank](https://github.com/tm-frank) |
| Henk Haarsma | Noordhoff Uitgevers | Member Technical Track | [@hhaarsma](https://github.com/hhaarsma) |
| Jan-Paul Mannee | Osingadejong | Member Technical Track | [@jpmannee](https://github.com/jpmannee) |
| Jorim van den Wijngaard | Topicus Education | Member Technical Track | [@jorimvdw](https://github.com/jorimvdw) |
| Kees van Ginkel | Iddink Group | Member Technical Track | [@mcginkel](https://github.com/mcginkel) |
| Koen Voermans | Stichting SEM | Project Manager and Lead Technical Track | [@kvoer](https://github.com/kvoer) |
| Luke Niesink | Topicus Education | Member Technical Track | [@niesink](https://github.com/niesink) |
| Marc Wijma | Boom VO | Member Technical Track | [@mwijma](https://github.com/mwijma) |
| Sieger Kuik | Stichting SEM | Lead Administrative Track | [@SiegerKuik](https://github.com/siegerkuik) |
