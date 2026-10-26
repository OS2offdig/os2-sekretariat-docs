---
title: Skabeloner
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 70
has_children: false
has_toc: true
---

# Skabeloner til arrangementer og mails
{: .no_toc }

> ✅ **Du kan som regel bruge OS2's eksisterende skabeloner**
>
> Skal du oprette et webinar eller et fysisk arrangement? Så kan du normalt nøjes med at vælge en af OS2's arrangementsskabeloner:
>
> - **OS2 webinar skabelon**
> - **OS2 fysisk arrangement skabelon**
>
> De almindelige spørgsmål og automatiske mails er allerede sat op. Du behøver derfor ikke oprette dine egne skabeloner.
>
> Husk blot at udfylde oplysningerne for dit arrangement – herunder mødelinket ved webinarer.
>
> **Brug Tjekliste til arrangementer i sidemenuen**, hvis du bare skal oprette et arrangement.

Denne vejledning er til dig, der har særlige behov og derfor vil oprette dine egne skabeloner.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Hvad er forskellen på skabelonerne?

Odoo bruger to forskellige slags skabeloner:

### Arrangementsskabelon

Bestemmer, hvordan et nyt arrangement sættes op fra starten.

Den kan blandt andet indeholde:

- spørgsmål til deltagerne
- automatiske mails og deres udsendelsestidspunkter
- andre faste indstillinger

**Eksempel:** Når du vælger OS2 webinar skabelon, får dit arrangement automatisk de almindelige spørgsmål og tre automatiske mails.

### Mailskabelon

Bestemmer, **hvad der står i en mail**.

En mailskabelon kan fx indeholde tekst til en bekræftelsesmail eller påmindelse. Den kan hente oplysninger om det konkrete arrangement automatisk.

**Eksempel:** Bekræftelsesmailen indsætter automatisk deltagerens navn, arrangementets titel og dato.

### Hvad bestemmer, hvornår mailen sendes?

På det enkelte arrangement finder du fanen **Kommunikation**.

Her kan du ændre udsendelsestidspunktet ved hjælp af **Interval, Enhed og Trigger**, uden at ændre indholdet i mailskabelonen eller påvirke andre arrangementer.

## Hvornår har du brug for en ny skabelon?

### Opret din egen mailskabelon, hvis:

- du ønsker en anden tekst i bekræftelsesmailen eller påmindelserne
- du vil sende en ekstra automatisk mail med særligt indhold
- et produkt skal have sin egen faste mailtekst til flere arrangementer

Du behøver ikke oprette en ny arrangementsskabelon, bare fordi du har brug for en anden mailtekst.

### Opret din egen arrangementsskabelon, hvis:

- du ofte opretter arrangementer med den samme særlige opsætning
- et produkt har brug for andre faste spørgsmål og automatiske mails
- flere personer skal kunne oprette samme type arrangement med en fælles opsætning

**Du behøver ikke nye skabeloner**, bare fordi dato, tidspunkt, adresse eller mødelink er anderledes. De oplysninger angives på det enkelte arrangement.

> ⚠️ **Ret ikke i OS2's fælles skabeloner**
>
> Du må ikke ændre indholdet i OS2's fælles mailskabeloner eller opsætningen af de fælles arrangementsskabeloner.
>
> Ændringer i en fælles mailskabelon kan påvirke mails til andre arrangementer. Ændringer i en fælles arrangementsskabelon kan påvirke opsætningen af nye arrangementer.
>
> Har du særlige behov, skal du oprette din egen skabelon.

## Opret en arrangementsskabelon

1. Gå til **Arrangementer → Konfiguration → Arrangementsskabeloner**.
2. Klik på **Ny**.
3. Giv skabelonen et tydeligt navn, fx `OS2produkt – workshop`.
4. Udfyld de indstillinger, der skal bruges igen.

Du kan blandt andet opsætte:

- **Kommunikation:** Automatiske mails og udsendelsestidspunkter.
- **Spørgsmål:** De oplysninger, deltagerne skal udfylde.
- **Billetter:** Eventuelle billettyper.
- Andre faste indstillinger efter behov.

Når du vælger skabelonen på et nyt arrangement, bruges dens opsætning som udgangspunkt.

## Opret en mailskabelon

Hvis du har brug for en særlig mailtekst:

1. Åbn et arrangement i Odoo.
2. Find fanen **Kommunikation** nederst.
3. Klik på **Tilføj en linje**.
4. Vælg **Mail**.
5. Klik i feltet, hvor mailskabelonen vælges.
6. Vælg **Søg flere...** og derefter **Opret nye**.
7. Giv mailskabelonen et tydeligt navn, og skriv mailen.
8. Gem og vælg skabelonen til din automatiske mail.

Giv gerne skabelonen et navn, der viser, hvad den skal bruges til, fx:

`OS2produkt: påmindelse til workshop`

Så kan andre se, hvem skabelonen hører til.

### Brug automatiske oplysninger i mailen

En mailskabelon kan automatisk hente oplysninger om:

- deltagerens navn
- arrangementets titel
- dato og tidspunkt
- sted og adresse
- URL til onlinearrangement

Det kaldes **dynamiske felter**.

Når du opretter en mailskabelon, der skal genbruges, bør du bruge dynamiske felter i stedet for at skrive fx en bestemt dato, by eller et mødelink direkte ind i teksten.

Brug Odoos funktion til at indsætte dynamiske felter, og kontrollér, at de viser de rigtige oplysninger.

> ⚠️ **Undgå faste mødelinks i mailskabeloner**
>
> Hvis du skriver et konkret Teams- eller mødelink direkte ind i en genbrugelig mailskabelon, risikerer du, at samme link bliver sendt til deltagere i andre arrangementer.
>
> Brug i stedet feltet **URL til onlinearrangement** på selve arrangementet og et dynamisk felt i mailskabelonen.

## Pas på, når du åbner en eksisterende mailskabelon

På et arrangement kan du åbne den valgte mailskabelon via den lille pil ved skabelonens navn under **Kommunikation**.

**Du åbner selve mailskabelonen – ikke en kopi til dit arrangement.**

Hvis du ændrer indholdet, kan ændringen derfor påvirke alle de arrangementer, der bruger skabelonen.

Ret ikke i OS2's fælles mailskabeloner. Opret din egen, hvis du har brug for andet indhold.

### Test din mailskabelon

Inden du tager en ny mailskabelon i brug, bør du kontrollere, at tekst og automatiske oplysninger vises korrekt.

> 💡 **Forhåndsvisning kan være misvisende**
>
> Odoo kan vise oplysninger fra et andet arrangement i forhåndsvisningen, fordi den bruger eksisterende tilmeldinger som eksempler.
>
> Du kan teste den faktiske mail ved at lave en testtilmelding til dit eget arrangement, når det er offentliggjort.

## Mere hjælp til Odoo

Se [Odoos officielle dokumentation](https://www.odoo.com/documentation/).

Vær opmærksom på, at menuer og funktioner kan variere mellem Odoo-versioner.
