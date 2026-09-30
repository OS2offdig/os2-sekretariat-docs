---
title: Skabeloner til arrangementer og mails
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 50
has_children: false
has_toc: true
---

# Skabeloner til arrangementer og mails
{: .no_toc }

Denne vejledning er relevant, hvis du vil oprette eller vedligeholde skabeloner, som skal kunne bruges igen.

Hvis du bare skal oprette ét arrangement med OS2's standardskabeloner, behøver du normalt ikke denne vejledning.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## To slags skabeloner

Odoo bruger to forskellige slags skabeloner:

**Arrangementsskabeloner** hjælper med opsætningen af selve arrangementet. De kan blandt andet indeholde spørgsmål og automatiske mails.

**Mailskabeloner** indeholder teksten i de mails, der kan sendes automatisk fra et arrangement.

Hos OS2 findes allerede to arrangementsskabeloner:

- **OS2 fysisk arrangement skabelon**
- **OS2 webinar skabelon**

De dækker de fleste almindelige arrangementer.

## Hvornår giver en ny skabelon mening?

Brug som udgangspunkt en af OS2's eksisterende skabeloner:

- **OS2 fysisk arrangement skabelon**
- **OS2 webinar skabelon**

De dækker de fleste almindelige arrangementer.

✅ **Lav kun en ny skabelon, hvis de eksisterende ikke passer godt nok.**

Det kan fx være, hvis:

- et produkt har brug for andre faste mails
- et produkt har brug for andre faste spørgsmål
- samme særlige opsætning skal bruges igen flere gange
- flere personer skal kunne oprette den samme type arrangement med en fast opsætning

En skabelon behøver ikke være fælles for hele OS2. Et produkt kan godt have sin egen, hvis der er et reelt behov.

❌ **Lav ikke en ny skabelon**, bare fordi:

- datoen er anderledes
- tidspunktet er anderledes
- stedet er anderledes
- mødelinket er anderledes

De oplysninger hentes fra det konkrete arrangement.

> 💡 **Hold antallet nogenlunde overskueligt**
>
> Skabeloner sparer tid, når de bliver genbrugt. For mange næsten ens skabeloner gør det til gengæld sværere at vælge den rigtige.

## Opret en arrangementsskabelon

Gå til:

**Arrangementer → Konfiguration → Arrangementsskabeloner**

Klik på **Ny**.

Giv skabelonen et navn, der gør det tydeligt, hvem og hvad den er til.

På skabelonen kan du blandt andet sætte:

- tidszone
- eventuel begrænsning på antal deltagere
- billetter
- automatiske mails under **Kommunikation**
- spørgsmål under **Spørgsmål**
- noter

Hos OS2 er det især **Kommunikation** og **Spørgsmål**, der er nyttige at sætte op på forhånd.

Når skabelonen senere vælges på et nyt arrangement, bruges dens opsætning som udgangspunkt. Det konkrete arrangement kan derefter tilpasses.

## Opret en mailskabelon

En mailskabelon er teksten, som en automatisk mail bruger.

Den letteste vej til at oprette en ny mailskabelon fra et arrangement er:

1. Åbn arrangementet.
2. Find fanen **Kommunikation** nederst på siden.
3. Klik på **Tilføj en linje**.
4. Vælg **Mail**.
5. Klik i feltet, hvor mailskabelonen vælges.
6. Vælg **Søg flere...**.
7. Klik på **Opret nye**.
8. Giv skabelonen et tydeligt navn og skriv mailen.

Når skabelonen er oprettet, kan den vælges på den automatiske mail.

Brug gerne et navn, der gør formålet tydeligt, fx:

`OS2produkt: påmindelse til workshop`

Så er det lettere for andre at se, om skabelonen er fælles, produktspecifik eller lavet til et særligt formål.

## Brug dynamiske oplysninger, når det er muligt

En mailskabelon kan hente oplysninger fra det arrangement, den bruges på.

Det kan fx være:

- deltagerens navn
- arrangementets navn
- dato og tidspunkt
- sted
- URL til onlinearrangement

Det betyder, at du normalt ikke behøver skrive konkrete datoer, adresser eller mødelinks direkte ind i en skabelon, der skal genbruges.

OS2's webinar-skabeloner henter fx mødelinket fra feltet **URL til onlinearrangement**.

> ⚠️ **Indsæt ikke et konkret mødelink i en fælles skabelon**
>
> Hvis du skriver et bestemt Teams- eller mødelink direkte ind i mailskabelonen, vil det samme link blive brugt alle de steder, hvor skabelonen bruges.

## Pas på, når du redigerer en mailskabelon

På et arrangement kan du åbne den valgte mailskabelon via den lille pil ved skabelonens navn.

Pilen kan være meget let at overse.

> ⚠️ **Du redigerer selve skabelonen**
>
> En mailskabelon kan bruges af flere arrangementer.
>
> Hvis du ændrer teksten i skabelonen, kan ændringen derfor slå igennem alle de steder, hvor den bruges.
>
> Skal teksten kun gælde ét arrangement, så opret en ny mailskabelon i stedet.

Det gælder også, selvom du åbner skabelonen fra fanen **Kommunikation** på ét bestemt arrangement.

## Arrangementsskabelon eller mailskabelon?

En enkel huskeregel:

**Arrangementsskabelon = hvordan arrangementet starter.**

**Mailskabelon = hvad der står i mailen.**

På det konkrete arrangement bestemmer **Interval, Enhed og Trigger**, hvornår mailen bliver sendt.

Se **Automatiske mails** for hjælp til at bruge og tilpasse de automatiske mails på et arrangement.

## Mere hjælp til Odoo

Odoo har også sin egen [dokumentation](https://www.odoo.com/documentation/).

Find **Events** under Odoos dokumentation, hvis du har brug for flere detaljer om skabeloner og arrangementer.

> 💡 **Tjek Odoo-versionen**
>
> Sørg for, at den vejledning, du læser hos Odoo, passer til den version, som os2.eu kører på. Menuer og muligheder kan ændre sig mellem versioner.
