# School Information System (SIS)

A service that allows an [Administrator](../roles/administrator.md) to manage the core data that the school needs to operate:  students, teachers, subjects, streams and classes.  This data is then provided (at the minimum level required and under the control of the school) to other services to allow them to function efficiently.  The SIS can also optionally fulfil the role of [Identity Provider](../identity-provider.md) for a school.

## Roles Related

  - [Administrator](../roles/administrator.md)
  - [LMC](../roles/lmc.md)

## Use Cases Related

- [S.2.0 Administrator establishes relationship between SIS, LMS and Marketplace](../use-cases/s.2.0-sims-lms-marketplace-setup.md)
- [S.3.0 Administrator connects purchased Learning Application, SIS and LMS](../use-cases/s.3.0-sims-lms-learning-application-setup.md)


## Data definitions
deatiled definitions can be found in the openapi spec : [SIS Data](https://stichtingsem.stoplight.io/docs/sem-technology-prototype/reference/sisdata.v1.yaml)

### Student
The student describes the student on a school in a particular schoolyear.
![Student](..\diagrams\SIS-Entity-Diagram-Student.drawio.svg)

### Teacher
The Teacher describes the teacher on a school in a particular schoolyear.
![Student](..\diagrams\SIS-Entity-Diagram-Teacher.drawio.svg)

### Group
The Group describes the groups (classes) on a school in a particular schoolyear.
![Student](..\diagrams\SIS-Entity-Diagram-Group.drawio.svg)

### Subject Choice
The subject choice is a combination of a subject (match), on a certain educational offering (eg HAVO), in a level (HAVO-1). It also contains the official government code for the subject and the name of the subject as is is used in the school
