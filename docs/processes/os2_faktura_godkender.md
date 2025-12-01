---
title: Fakturagodkender
layout: default
parent: Processer og rutiner
nav_order: 2
---

# Oversigt over hvem der godkender regninger

| PSP-element   | Projektnavn       | Intern godkender                 | Ekstern godkender                             |
|---------------|-------------------|----------------------------------|-----------------------------------------------|
| XG-4300001222 | OS2kravmotor      | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Line Lynggaard Sørensen [lils@syddjurs.dk](mailto:lils@syddjurs.dk)      |
| XG-4300001223 | OS2rollekatalog   | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Mette Valbjørn [metva@favrskov.dk](mailto:metva@favrskov.dk)              |
| XG-4300001224 | OS2autoproces     | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Ny på vej                                     |
| XG-4300001225 | OS2indberetning   | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Katrine Kjærgaard Bach [katrine.k.bach@rksk.dk](mailto:katrine.k.bach@rksk.dk) |
| XG-4300001226 | OS2valghalla      | Lisbeth Lorentzen [liwl@aarhus.dk](mailto:liwl@aarhus.dk) | Koordinationsgruppen                          |
| XG-4300001227 | OS2faktor         | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Jens Andreas Kristensen [dres@rksk.dk](mailto:dres@rksk.dk)          |
| XG-4300001228 | OS2udoglær        | Mie Frydensbjerg [mif@aarhus.dk](mailto:mif@aarhus.dk)   | Ingen                                         |
| XG-4300001230 | OS2flytjord       | Mette Hansen [meeh@aarhus.dk](mailto:meeh@aarhus.dk)      | Koordinationsgruppen                          |
| XG-4300001231 | OS2kle            | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Ingen                                         |
| XG-4300001232 | OS2sync           | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Ingen                                         |
| XG-4300001233 | OS2forms          | Anna-Lis Berg [besoan@aarhus.dk](mailto:besoan@aarhus.dk)   | Koordinationsgruppen                          |
| XG-4300001234 | OS2borgerPC       | Anna-Lis Berg [besoan@aarhus.dk](mailto:besoan@aarhus.dk)   | Koordinationsgruppen                          |
| XG-4300001235 | OS2display        | Anna-Lis Berg [besoan@aarhus.dk](mailto:besoan@aarhus.dk)   | Koordinationsgruppen                          |
| XG-4300001236 | OS2iot            | Lisbeth Lorentzen [liwl@aarhus.dk](mailto:liwl@aarhus.dk) | Koordinationsgruppen                          |
| XG-4300001238 | OS2mo             | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Mikael Olsen [miol@balk.dk](mailto:miol@balk.dk)                     |
| XG-4300001239 | OS2kitos          | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Mikael Olsen [miol@balk.dk](mailto:miol@balk.dk)                     |
| XG-4300001240 | OS2skoledata      | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Lars Lyngsøe Højberg [ilahn@rebild.dk](mailto:ilahn@rebild.dk)          |
| XG-4300001241 | OS2sofd           | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Erling Haunstrup Poulsen [ehp@syddjurs.dk](mailto:ehp@syddjurs.dk)      |
| XG-4300001242 | OS2compliance     | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Nina Birthe Sørensen [nina@nibis.dk](mailto:nina@nibis.dk)            |
| XG-4300001243 | OS2skadesøkonomi  | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Lars Kaalund [laka@kl.dk](mailto:laka@kl.dk)                       |
| XG-4300001244 | OS2korrespondance | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Michelle Juhl [mjbp@syddjurs.dk](mailto:mjbp@syddjurs.dk)                |
| XG-4300001245 | OS2nectar         | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Jens Kjellerup [jeh2@balk.dk](mailto:jeh2@balk.dk)                   |
| XG-4300001246 | OS2skole          | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Henrik Bojsen [heboj@syddjurs.dk](mailto:heboj@syddjurs.dk)               |
| XG-4300001247 | OS2fleetoptimiser | Sofie Buhl [sofbu@aarhus.dk](mailto:sofbu@aarhus.dk)       | Ingen                                         |
| XG-4300001248 | OS2planCO2        | Rasmus Frey [rafr@aarhus.dk](mailto:rafr@aarhus.dk)       | Ingen                                         |
| XG-4300001249 | OS2ai             | Signe Marie Skovby Ahm [masia@aarhus.dk](mailto:masia@aarhus.dk) | Ingen                                   |
| XG-4300001250 | OS2connector      | Sofie Buhl [sofbu@aarhus.dk](mailto:sofbu@aarhus.dk)       | Ingen                                         |

## Proces for godkendelse af faktura i OS2

```mermaid
flowchart TD
    A[Intern godkender modtager faktura] --> B{Kan der godkendes direkte?}
    B -->|Ja| C[Godkender betaling]
    B -->|Nej| D[Sender mail til ekstern godkender]
    D --> E{Modtager svar}
    E -->|Ja| F[Godkender betaling]
    E -->|Nej| G[Iteration til vi har en endelige konklusion] -->D
```