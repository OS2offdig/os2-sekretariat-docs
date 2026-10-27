---
title: Opret selv et arrangement
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 30
has_children: false
has_toc: true
---

# Opret selv et arrangement i Odoo
{: .no_toc }

Denne vejledning er til dig, der har adgang til Odoo og selv skal oprette et arrangement på os2.eu.

**Start med en af OS2's arrangementsskabeloner.** Så er de almindelige spørgsmål og automatiske mails allerede sat op.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## 1. Opret arrangementet

Gå til **Arrangementer** i Odoo, og klik på **Ny**.

Udfyld arrangementets titel, dato og start- og sluttidspunkt.

### Vælg en skabelon

Find feltet **Skabelon** øverst på siden. Feltet kan være let at overse.

Vælg:

- **OS2 fysisk arrangement skabelon** ved fysiske arrangementer
- **OS2 webinar skabelon** ved onlinearrangementer

Skabelonen sørger blandt andet for, at standardspørgsmål og automatiske mails bliver sat op.

Udfyld derefter:

- **Arrangør**
- **Ansvarlig**
- **Sprog** – vælg gerne Dansk
- eventuelle **Tags**

## 2. Angiv sted eller mødelink

### Fysisk arrangement

Vælg arrangementets **Lokale**, og kontrollér adressen.

### Webinar

Ved webinarer skal feltet **Lokale** være tomt.

Når du fjerner et lokale, får du mulighed for at udfylde **URL til onlinearrangement**.

Indsæt dit Teams- eller andet mødelink her.

> ⚠️ **Husk mødelinket!**
>
> OS2's automatiske webinar-mails henter mødelinket fra feltet **URL til onlinearrangement**.
>
> Indsæt derfor linket, inden du åbner for tilmelding.

## 3. Vælg synlighed

Under **Synlighed** vælger du, hvordan arrangementet kan findes på hjemmesiden.

Du kan blandt andet vælge, at arrangementet kun skal kunne findes via et direkte link.

**Overvej, om arrangementet bør være synligt for alle.** Det kan godt være relevant at vise et arrangement på hjemmesiden, selvom det kun er for en bestemt målgruppe.

Brug derfor kun visning via link, hvis der er en konkret grund til det.

## 4. Indstil deltagerantal og tilmeldingsfrist

### Begræns antal deltagere

Er der et begrænset antal pladser, skal du slå **Begræns tilmeldinger** til og angive det maksimale antal.

### Angiv en tilmeldingsfrist

Vil du have tilmeldingen til at lukke automatisk på et bestemt tidspunkt, gør du sådan:

1. Gå til fanen **Billetter** nederst på arrangementet.
2. Hvis der ikke allerede er en billet, klik på **Tilføj en linje**, og opret en. Du kan bruge Odoos foreslåede standardopsætning.
3. Giv eventuelt billetten et navn, fx *Tilmelding*. Kontrollér, at prisen er 0 kr., hvis arrangementet er gratis.
4. Angiv dato og klokkeslæt i feltet **Registrering Slut**.
5. Gem ændringen.

Når fristen er passeret, lukker tilmeldingen via billetten automatisk.


## 5. Tjek spørgsmålene ved tilmelding

Nederst på arrangementet finder du fanerne:

**Billetter · Kommunikation · Spørgsmål · Noter og dokumenter**

Vælg **Spørgsmål**.

OS2's skabeloner indeholder som udgangspunkt:

- navn
- e-mail
- organisation

Du kan tilføje flere spørgsmål efter behov, fx om kosthensyn, rolle eller fagområde.

Du kan også vælge, om et spørgsmål skal være obligatorisk.

### Hvis arrangementet kun er for en bestemt målgruppe

Du kan tilføje et obligatorisk spørgsmål, hvor deltageren bekræfter at tilhøre målgruppen.

Eksempel:

"Jeg bekræfter, at jeg er en del af OS2[produkt]-fællesskabet."

**Bemærk:** Odoo kontrollerer ikke automatisk, om deltageren opfylder betingelserne. Arrangøren skal selv kontrollere tilmeldingerne.


## 6. Tjek de automatiske mails

Vælg fanen **Kommunikation** nederst på arrangementet.

Når du bruger en af OS2's arrangementsskabeloner, er de almindelige automatiske mails allerede sat op. Du behøver derfor ikke gøre mere, medmindre du har særlige behov.

**Vil du ændre udsendelsestidspunktet?**

Du kan ændre **Interval, Enhed og Trigger** under Kommunikation på dit eget arrangement.

Det påvirker ikke de fælles mailskabeloner eller andre arrangementer.

**Husk:** Kontrollér, at mailens tekst stadig passer til det nye udsendelsestidspunkt.

> ⚠️ **Ret ikke indholdet i de fælles mailskabeloner**
>
> Ændringer i en fælles mailskabelon kan påvirke andre arrangementer.
>
> Har du brug for en anden mailtekst eller ekstra automatiske mails med særligt indhold, skal du oprette dine egne mailskabeloner.


### Tags (valgfrit)

Hvis arrangementet hører til et bestemt OS2-produkt, kan du tilføje produktets tag.

Tags gør det muligt at lave en arrangementsoversigt på produktets side på os2.eu, som kun viser arrangementer for det pågældende produkt – ligesom med blogindlæg.

Det er især en fordel for produkter, der løbende annoncerer arrangementer.


## 7. Gå videre til arrangementssiden

Når oplysningerne er på plads, kan du fortsætte med at opsætte selve arrangementssiden på os2.eu.

Husk, at arrangementet også skal offentliggøres, før deltagere kan tilmelde sig via hjemmesiden.

## Mere hjælp til Odoo

Har du brug for mere hjælp, kan du bruge Odoos officielle dokumentation om Events.

Vær opmærksom på, at menuer og funktioner kan variere mellem Odoo-versioner.
