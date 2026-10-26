---
title: Automatiske mails
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 60
has_children: false
has_toc: true
---

# Automatiske mails
{: .no_toc }

> ✅ **Har du brugt en af OS2's arrangementsskabeloner? Så er de automatiske mails allerede sat op!**
>
> Bekræftelsesmail og påmindelser er sat op på forhånd. Du behøver hverken oprette, tilknytte eller redigere mailskabeloner.
>
> **Gå videre til Tjekliste til arrangementer i sidemenuen**, og kontrollér, at resten af dit arrangement er klar.
>
> **Husk ved webinarer:** Du skal selv indsætte mødelinket i feltet **URL til onlinearrangement** på arrangementet.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Vigtigt om fælles mailskabeloner

> ⚠️ **Ret ikke indholdet i OS2's fælles mailskabeloner**
>
> De fælles mailskabeloner bruges af flere arrangementer. Hvis du ændrer teksten, kan det påvirke mails til andre arrangementer.
>
> **Har du brug for en anden mailtekst?** Opret din egen mailskabelon i stedet.
>
> **Du må gerne ændre udsendelsestidspunktet** under fanen **Kommunikation** på dit arrangement. Det ændrer ikke i den fælles mailskabelon og påvirker ikke andre arrangementer.

Resten af vejledningen er til dig, der vil vide mere om de automatiske mails eller har brug for at tilpasse dem til et særligt arrangement.

## Hvilke mails følger med?

### OS2 webinar skabelon

Der følger tre automatiske mails med:

- **Webinar: bekræftelse på tilmelding (OS2)** – sendes efter tilmelding
- **Webinar: påmindelse 2 dage før (OS2)**
- **Webinar: påmindelse 2 timer før (OS2)**

Mailsene henter automatisk oplysninger fra arrangementet, fx:

- deltagerens navn
- arrangementets titel
- dato og tidspunkt
- mødelink
- kalenderlinks

**Mødelinket hentes fra feltet URL til onlinearrangement på selve arrangementet.** Du må derfor ikke indsætte mødelinket i mailskabelonen (medmindre du opretter din egen).

### OS2 fysisk arrangement skabelon

Der følger også tre automatiske mails med:

- **Fysisk arrangement: bekræftelse på tilmelding (OS2)** – sendes efter tilmelding
- **Fysisk arrangement: påmindelse 2 dage før (OS2)**
- **Fysisk arrangement: påmindelse 12 timer før (OS2)**

Mailsene henter automatisk oplysninger om arrangementet, herunder navn, dato, tidspunkt og sted.

## Find de automatiske mails

1. Åbn arrangementet i Odoo.
2. Find fanen **Kommunikation** nederst på siden.

Her kan du se, hvilke mails der er tilknyttet arrangementet, og hvornår de sendes.

> 💡 **Hvad er forskellen?**
>
> **Den automatiske mail** bestemmer, hvornår mailen sendes.
>
> **Mailskabelonen** bestemmer, hvad der står i mailen.

## Hvornår har du brug for din egen mailskabelon?

Du behøver kun oprette en ny mailskabelon, hvis du har brug for en anden tekst end den, der følger med OS2's skabeloner.

Det kan fx være, hvis:

- et produkt ønsker en særlig mailtekst til sine arrangementer
- et arrangement kræver ekstra information i bekræftelsen eller påmindelserne
- du vil tilføje en ekstra automatisk mail med sit eget indhold

**Du behøver ikke en ny mailskabelon**, bare fordi arrangementet har en anden dato, adresse eller et andet mødelink. De oplysninger hentes automatisk fra arrangementet.

## Ændr tidspunktet for en automatisk mail

Du kan ændre, hvornår de automatiske mails sendes, på dit eget arrangement. Det påvirker ikke den fælles mailskabelon eller andre arrangementer.

1. Åbn arrangementet i Odoo.
2. Gå til fanen **Kommunikation**.
3. Find den mail, du vil ændre tidspunktet for.
4. Justér de relevante felter:
   - **Interval** – hvor lang tid før eller efter
   - **Enhed** – fx timer eller dage
   - **Trigger** – hvilken hændelse tidspunktet beregnes ud fra

Du kan fx ændre en påmindelse fra to dage før til én dag før.

> ⚠️ **Husk at kontrollere teksten**
>
> OS2's standardmails kan indeholde formuleringer som "vi ses om et par timer".
>
> Hvis du ændrer udsendelsestidspunktet, kan teksten derfor blive misvisende.
>
> Har du også brug for en anden tekst, skal du oprette din egen mailskabelon.

## Pas på, når du åbner en mailskabelon

Du kan åbne en mailskabelon via den lille pil ved skabelonens navn under **Kommunikation**.

**Vær opmærksom på, at du åbner selve mailskabelonen – ikke en kopi til dit arrangement.**

Du må derfor ikke ændre indholdet i OS2's fælles mailskabeloner.

> 💡 **Forhåndsvisning kan vise et andet arrangement**
>
> Når du forhåndsviser en mailskabelon, kan Odoo vise oplysninger fra et andet arrangement. Det skyldes, at forhåndsvisningen bruger eksisterende tilmeldinger som eksempler.
>
> Det betyder ikke nødvendigvis, at noget er galt.
>
> Hvis du vil kontrollere mailen til dit eget arrangement, kan du lave en testtilmelding med din egen mailadresse, når arrangementet er offentliggjort.

## Tilføj en automatisk mail

Hvis du har brug for en ekstra mail:

1. Åbn fanen **Kommunikation**.
2. Klik på **Tilføj en linje**.
3. Vælg **Mail**.
4. Vælg den mailskabelon, du vil bruge. Vælg eventuelt **Søg flere...**, hvis du ikke kan finde den.
5. Angiv **Interval**, **Enhed** og **Trigger**.

Har du brug for en anden mailtekst, skal du først oprette din egen mailskabelon.

## Mere hjælp til Odoo

Se [Odoos officielle dokumentation](https://www.odoo.com/documentation/).

Vær opmærksom på, at menuer og funktioner kan variere mellem Odoo-versioner.
