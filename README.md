# SEM Ecosytem Standard

## Note: Legal status of the specifications in this repository
 > All information in this repository is draft. No rigths can be claimed based on this information
 > The standards can change without notice until they are finalised and approved

## Abstract

A typical school uses a broad range of learning materials from several educational publishers or educational platform suppliers. The SEM Ecosystem sets a standard for the exchange of data between all parties that play a key role in the order and access of these (digital) learning materials within schools. Parties involved are amongst others providers of student information systems, learning managemenst systems, distribution and fulfillment, and (digital) learning materials.

## Structure of this repository

This repository consists of the following elements:
- [Beginner's Guide](beginners-guide.md) which explains all the concepts within the ecosystem in more detail.
- [Technical reference](technical-reference.md) with information about the architecture, used standards and links to the reference files.
- [API documentation](https://stichtingsem.stoplight.io/) can be found on stoplight
- [Implementation Guide](implementation-guide.md) with practical advice for new parties.
- [Glossary](glossary.md) describing all terms and definitions used within the ecosystem

This repository is an initiative of the Stichting Samenwerkende Educatieve Marktpartijen (SEM) and is based upon the principles defined in the working document [Moving from a chain to an ecosystem](documentation/documents/).

## Moving from a chain to an ecosystem

Stichting Samenwerkende Educatieve Marktpartijen (SEM) is a foundation where private parties work together. Within a large group of organizations there exists the wish to simply the way all parties work together in order to deliver (digital) learning materials to the end-users within Dutch schools. This was the reason to start an investigation both on CEO as on CTO level how this can be achieved. The investigation resulted in the design of a new technical standard: the SEM ecosystem.

The SEM ecosystem tries to overcome the main challenges in the current learning materials chain (leermiddelenketen in Dutch):
- The current chain is build upon principles of the supply of physical learning materials. Moreover, administrative processes are leading. This leads to issues in the immediate access to digital learning materials.
- There is a large dependency between parties within the current chain. On the other hand is the use of standards and the commitment to industry agreements open-ended. Parties are therefore able to (not) use these standards and agreements without obligation.
- The current chain is too complex for the end-users within schools.
- The technology used within the current chain is end-of-life.

## Purpose of the SEM ecosystem: 10 times better

The SEM ecosystem solves the challenges of the current learning materials chain and improves the supply and access of learning materials on ten goals.

| # | Goals | Current | Proposed solution | Beneficiary |
|:---:|---|---|---|---|
| 1 | Immediate Access to digital material | - Current system does not allow immediate access. In most cases access is dependent on upfront payment and/or the physical delivery of folio components (in case of hybrid products) | - Immediate access for users is guaranteed by entitlements (on the highest possible level such as a school)<br>    - No direct relations with stock levels and availability folio component<br>    - Schools control access through the LMS. Data is directly shared with connected partners (MP)<br>    - Possible access issues are dealt with in front  | Pupil/Student,Teachers, School boards, LMC, MP, LA |
| 2 | Dynamic Learning | - In the current system materials are bought for a schoolyear based on a LML compiled before the start of the school year. This is a static process<br>- Schools are typically connected to and dependent on specific partners | - Ecosystem enables dynamics learning<br>    - Learning material can be bought based on LML, but also on the wider catalogue presented in the LMS<br>    - Teachers can promote learning material in the LMS for immediate access<br>    - Entitle on group and/or individual level<br>    - Technical solution is flexible and can be used to support all kinds (not only ECK material)<br>    - Schools can be connected to multiple marketplaces and  LMS’s at the same time | Pupil/Student, Teacher, LMC, School Boards |
| 3 | Easy setup | - Schools are not in control due to un transparency of the system and the data transported between partners | - IT administrators can do setups themselves instead of hiring brokers and other IT company’s<br>    - Setup connections from LMS to marketplace and learning applications will be easy to achieve like for example the configuration of Office 365 accounts<br>    - Schools at at all times in control due to increased transparency | IT Administrator (Schools), LMC, SIS |
| 4 | Various business models | - The current system only supports business models based on transaction | - The ecosystem supports business models based on payment (transaction) or usage (subscription).<br>    - Examples: Subscription, Pre-paid, Post-paid, Free content, Freemium, etc. | LA, MP, School boards |
| 5 | Low threshold | - Current system is too complex for new partners to enter | - The new ecosystem is easy to enter for new partners because of its low complexity<br>    - Less, transparent, discoverable services based on role(s)<br>    - Technical solution is well documented | LMS, MP, LA |
| 6 | Increase trust | - Limited actual information available<br>- Untransparent processes<br>- Mistrust between chain partners | - Schools and connected partners have more and actual informationin the ecosystem<br>    - Information will be shared immediately on predefined events<br>    - Support will be easier because of the available information | MP. LA, School Boards |
| 7 | Transparent transactions and balanced administrations | - Untransparency: due to the complexity of the chain there are often disagreements (# licenses sold, # license stock) | - In the new ecosystem administration follows usage, but balanced administrations are ensured<br>    - Market places establish entitlements at learning applications based on SIS/LMS data<br>    - Entitlements are available for involved partners and are the base for valid transactions | LMC, LMS, MP, LA, School Boards |
| 8 | Less central services | - Strong dependency on central services (Edu iX) and Lika’s | - Limited dependencies to central services<br>    - Connections are setup directly between partners in the ecosystem (decentral services) | SIS, LMS, ITAdministrator (School) |
| 9 | Compliance (security & privacy) | - Although attempts have been made and will be made to minimalize data this will remain difficult in the current chain due to the complexity | - The ecosystem ensures data minimisation<br>    - Transactions take place on identifiers for products, schools, users, market place<br>- School (IT administrator) manage the access and right to data in the SIS/LMS<br>    - Data is shared based on role (target binding).<br>    - Personal data will only be shared after additional authentication | All |
| 10 | Futureproof technical solution | - The currently used technical standards like SAML and SOAP  are end of life cycle  | - The technical solution is based on modern and mature coding standards(events, webhooks, Oauth) | All |

## Version history

| Version | Date issues | Status | Author |
|---|---|---|---|
| 0.1 | 2 December 2021 | DRAFT | [@kvoer](https://github.com/kvoer) |
| 0.2 | 7 December 2021 | DRAFT | [@kvoer](https://github.com/kvoer) |

## Contributors

This standard is developed by members from [Stichting SEM](www.stichtingsem.org). The contributors to the SEM Ecosystem standard are:

| Name | Organization | Role | Alias |
|---|---|---|---|
| Clifton Cunningham | Infinitas Learning | Initiator | [@cliftonc](https://github.com/cliftonc) |
| Carl Verhoest | Infinitas Learning | Member Technical Track | |
| Danny Pronk | The Learning Network | Member Technical Track | [@dpronk](https://github.com/dpronk) |
| Elias Hassing | Infinitas Learning | Lead Functional Track | [@eliashassing154](https://github.com/eliashassing154) |
| Edwin Verwoerd | Iddink Group | Member Technical & Administrative Track | [@edwinverwoerd](https://github.com/edwinverwoerd) |
| Frank Aarts | ThiemeMeulenhoff | Member Technical Track | [@TM-Frank](https://github.com/tm-frank) |
| Henk Haarsma | Noordhoff Uitgevers | Member Technical Track | [@hhaarsma](https://github.com/hhaarsma) |
| Jan-Paul Mannee | Osingadejong | Member Technical Track | [@jpmannee]https://github.com/jpmannee|
| Jorim van den Wijngaard | Topicus Education | Member Technical Track | [@jorimvdw](https://github.com/jorimvdw) |
| Kees van Ginkel | Iddink Group | Member Technical Track | [@mcginkel](https://github.com/mcginkel) |
| Koen Voermans | Stichting SEM | Project Manager and Lead Technical Track | [@kvoer](https://github.com/kvoer) |
| Luke Niesink | Topicus Education | Member Technical Track | [@niesink](https://github.com/niesink) |
| Marc Wijma | Boom VO | Member Technical Track | [@mwijma]https://github.com/mwijma |
| Sieger Kuik | Stichting SEM | Lead Administrative Track | [@SiegerKuik](https://github.com/siegerkuik) |