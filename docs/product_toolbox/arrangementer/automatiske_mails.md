---
title: Automatiske mails
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 40
has_children: false
has_toc: true
---

# Automatiske mails
{: .no_toc }

Når du bruger en af OS2's arrangementsskabeloner, er de almindelige automatiske mails allerede sat op.

I de fleste tilfælde behøver du derfor ikke ændre noget.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Det får du med OS2's skabeloner

### OS2 webinar skabelon

Der følger tre mails med:

- **Webinar: bekræftelse på tilmelding (OS2)** – sendes efter tilmelding
- **Webinar: påmindelse 2 dage før (OS2)**
- **Webinar: påmindelse 2 timer før (OS2)**

Mailsene henter automatisk oplysninger fra arrangementet, fx:

- deltagerens navn
- arrangementets navn
- dato og tidspunkt
- mødelink fra **URL til onlinearrangement**
- kalenderlinks

Du skal altså **ikke indsætte det konkrete mødelink i mailskabelonen**.

Udfyld mødelinket på selve arrangementet. Så hentes det automatisk ind i mailen.

### OS2 fysisk arrangement skabelon

Der følger tre mails med:

- **Fysisk arrangement: bekræftelse på tilmelding (OS2)** – sendes efter tilmelding
- **Fysisk arrangement: påmindelse 2 dage før (OS2)**
- **Fysisk arrangement: påmindelse 12 timer før (OS2)**

Mailsene henter automatisk oplysninger fra arrangementet, fx navn, dato, tidspunkt og sted.

## Find de automatiske mails

Åbn arrangementet i Odoo.

Nederst på siden finder du fanen **Kommunikation**.

Her kan du se:

- hvilken mailskabelon der bruges
- hvornår mailen sendes
- hvad der udløser den

> 💡 **To ting, der hænger sammen**
>
> Den automatiske mail bestemmer **hvornår** mailen bliver sendt.
>
> Mailskabelonen bestemmer **hvad der står i mailen**.

## Skal du ændre noget?

Brug denne tommelfingerregel:

✅ **Brug OS2's eksisterende skabelon**, hvis standardmailen indeholder det, deltagerne skal vide.

✅ **Opret en ny mailskabelon**, hvis:

- et produkt gerne vil have sin egen faste mailtekst
- samme særlige tekst skal bruges til flere af produktets arrangementer
- ét konkret arrangement kræver indhold, som ikke passer i standardmailen

❌ **Opret ikke en ny mailskabelon**, bare fordi:

- datoen er anderledes
- stedet er anderledes
- mødelinket er anderledes

De oplysninger kan hentes automatisk fra arrangementet.

❌ **Ret ikke OS2's fælles mailskabelon** for at indsætte oplysninger om ét bestemt arrangement.

## Ændr hvornår en mail sendes

Du kan ændre **Interval, Enhed og Trigger** på det enkelte arrangement uden at ændre andre arrangementer.

Det betyder fx, at du kan ændre en påmindelse fra to dage før til én dag før.

> ⚠️ **Tjek teksten, hvis du ændrer tidspunktet**
>
> OS2's standardmails er skrevet til deres normale tidspunkt. Der kan fx stå *“vi ses om et par timer”* eller *“vi ses om et halvt døgns tid”*.
>
> Hvis du ændrer tidspunktet markant, kan teksten derfor blive misvisende.
>
> Har du brug for både et andet tidspunkt **og** en anden tekst, så opret en ny mailskabelon.

## Pas på, når du åbner en mailskabelon

Ved navnet på den valgte mailskabelon kan du åbne selve skabelonen via den lille pil.

Pilen kan være let at overse.

> ⚠️ **Du åbner selve mailskabelonen**
>
> Ændrer du teksten her, kan ændringen slå igennem alle de steder, hvor skabelonen bruges.
>
> Ret derfor kun en eksisterende skabelon, hvis ændringen skal gælde alle de arrangementer, der bruger den.
>
> Er teksten kun til ét arrangement, så opret en ny mailskabelon i stedet.

Se **Skabeloner til arrangementer og mails** for, hvordan du opretter en ny mailskabelon.

## Tilføj en automatisk mail

Hvis du har brug for en ekstra mail:

1. Åbn fanen **Kommunikation**.
2. Klik på **Tilføj en linje**.
3. Vælg **Mail**.
4. Klik i feltet til mailskabelonen.
5. Vælg den skabelon, du vil bruge.
6. Hvis du ikke kan finde den, vælg **Søg flere...**.
7. Angiv **Interval**, **Enhed** og **Trigger** for at bestemme, hvornår mailen skal sendes.

Hvis mailen kræver sin egen tekst, skal du oprette en ny mailskabelon.

Se **Skabeloner til arrangementer og mails**.

## Mere hjælp til Odoo

Denne vejledning beskriver den måde, vi bruger automatiske mails på i OS2.

Har du brug for flere detaljer, kan du også bruge [Odoos egen dokumentation](https://www.odoo.com/documentation/).

> 💡 **Tjek Odoo-versionen**
>
> Sørg for, at den vejledning, du læser hos Odoo, passer til den version, som os2.eu kører på. Menuer og muligheder kan ændre sig mellem versioner.
