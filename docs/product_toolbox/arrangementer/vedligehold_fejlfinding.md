---
title: Vedligehold og fejlfinding
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 80
has_children: false
has_toc: true
---

# Vedligehold og fejlfinding af arrangementer
{: .no_toc }

Denne vejledning er til dig, der har ansvar for at vedligeholde OS2's fælles arrangementsopsætning i Odoo.

Her samler vi løsninger på kendte problemer med arrangementer og skabeloner.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Fejl i automatiske mails

Hvis en automatisk mail indeholder forkerte oplysninger, skal du først undersøge, om fejlen ligger i arrangementets oplysninger eller i den fælles mailskabelon.

### 1. Kontrollér arrangementet

Åbn arrangementet i Odoo.

Kontrollér, at titel, dato, tidspunkt og sted er korrekte.

Ved webinarer skal du også kontrollere feltet **URL til onlinearrangement**.

Hvis oplysningerne er korrekte, kan fejlen skyldes mailskabelonen.

### 2. Find mailskabelonen

1. Åbn arrangementet.
2. Gå til fanen **Kommunikation**.
3. Find den automatiske mail, der er problemer med.
4. Klik på den lille pil ved mailskabelonens navn for at åbne skabelonen.

**Vigtigt:** Du åbner den fælles mailskabelon, som også kan bruges af andre arrangementer.

### 3. Kontrollér dynamiske felter

En mailskabelon skal kunne hente oplysninger fra det konkrete arrangement.

Det sker via **dynamiske felter**.

Odoo Support har anbefalet følgende udtryk til arrangementsoplysninger:

| Oplysning | Dynamisk felt |
|---|---|
| Arrangementets navn | `{{ object.event_id.name }}` |
| Startdato og tidspunkt | `{{ object.event_id.date_begin }}` |
| Adresse | `{{ object.event_id.address_inline }}` |
| Navn på arrangementssted | `{{ object.event_id.address_id.name }}` |

Vær opmærksom på:

- Dynamiske udtryk skal have dobbelte tuborgklammer: `{{ }}`.
- Brug ikke `object.event_id.address_search` til adressen. Odoo Support har identificeret dette som et forkert udtryk i den tidligere fejl.
- Kontrollér, at der ikke står faste stednavne, adresser eller datoer i en skabelon, som skal genbruges.
- Brug så vidt muligt Odoos editor til at indsætte dynamiske felter frem for at redigere kode direkte.

**Bemærk:** Datoer indsat direkte via tekniske udtryk kan få et uhensigtsmæssigt format med sekunder. Kontrollér derfor altid den færdige mail.

### 4. Test mailen

Når eventuelle fejl er rettet og ændringerne gemt:

1. Kontrollér mailen i Odoos forhåndsvisning.
2. Vær opmærksom på, at forhåndsvisningen kan bruge tilmeldinger fra et andet arrangement.
3. Lav en testtilmelding til et offentliggjort arrangement.
4. Kontrollér den mail, du modtager.

Tjek især titel, dato, tidspunkt, adresse og eventuelle mødelinks.

### 5. Kontrollér andre arrangementer

Hvis fejlen har været i en fælles mailskabelon, bør du også kontrollere de kommende arrangementer, der bruger den.

Åbn deres fane **Kommunikation**, og kontrollér, hvilke mailskabeloner der er tilknyttet.

## Ændring af udsendelsestidspunkt

Under **Kommunikation** på det enkelte arrangement kan du ændre **Interval, Enhed og Trigger**.

Det ændrer ikke indholdet i den fælles mailskabelon.

Hvis du ændrer tidspunktet, skal du dog kontrollere, at mailens tekst stadig passer.

## Hvis problemet ikke er løst

Kontakt Odoo Support med:

- navnet på arrangementet
- navnet på den berørte mailskabelon
- en beskrivelse af fejlen
- eventuelle screenshots og eksempler på forkerte mails

Odoos dokumentation om dynamiske felter:

https://www.odoo.com/documentation/20.0/applications/general/companies/email_template.html#dynamic-placeholders

Kontrollér, at dokumentationen passer til den Odoo-version, vi anvender.
