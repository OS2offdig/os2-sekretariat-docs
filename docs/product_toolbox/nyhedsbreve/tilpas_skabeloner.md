---
title: Tilpas en mailskabelon
layout: default
parent: Opsætning af nyhedsbrevsliste
grand_parent: Nyhedsbreve
nav_order: 60
has_children: false
has_toc: true
---

# Tilpas en mailskabelon i Heyloyalty
{: .no_toc }

OS2-sekretariatet har oprettet en grundskabelon, som er tilpasset de enkelte produkter. Denne vejledning er til dig, der opretter mailskabelonen til en ny nyhedsbrevsliste.

Du behøver normalt ikke ændre skabelonen, når du sender nyhedsbreve. Nyhedsbrevets indhold redigeres direkte i kampagnens editor. 

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

# Tilpas en mailskabelon i Heyloyalty

OS2 har en fælles grundskabelon til nyhedsbreve. Når et nyt produkt eller projekt skal have sin egen mailskabelon, kopierer du grundskabelonen og tilpasser nogle få oplysninger.

**Du skal kun rette tekst og links – ikke selve HTML-strukturen.**

## Trin 1: Opret en kopi

1. Gå til **Skabeloner** i Heyloyalty.
2. Find OS2's fælles grundskabelon.
3. Klik på de tre prikker (⋯), og vælg **Kopiér skabelon**.
4. Giv kopien et navn, fx `OS2ai – Nyhedsbrev`.
5. Åbn kopien, og vælg **Rediger skabelon**.

**Vigtigt:** Ret altid i kopien – ikke i den fælles grundskabelon.

## Trin 2: Tilpas skabelonen

Nu skal du rette seks steder i HTML-koden.

Brug søgefunktionen til at finde teksterne. Du kan også kopiere koden til en teksteditor, hvis det er nemmere.

Eksemplerne nedenfor bruger OS2ai. Erstat med det relevante produkt- eller projektnavn og den korrekte hjemmesideadresse.

### 1. Sidens titel

Find:

`<title>Nyheder fra OS2</title>`

Ret til:

`<title>Nyheder fra OS2ai</title>`

### 2. Header – nyhedsbrevets navn

Find teksten:

`Nyheder fra OS2`

Ret til:

`Nyheder fra OS2ai`

### 3. Footer – afsendernavn

Find:

`– Offentligt digitaliseringsfællesskab`

Tilføj produkt- eller projektnavnet, fx:

`– Offentligt digitaliseringsfællesskab · OS2ai`

**Lad resten af HTML-koden og den grønne OS2-tekst stå.**

### 4. Footer – hvorfor modtageren får mailen

Find teksten, der begynder:

`Du modtager denne e-mail, fordi du er tilmeldt`

Ret teksten til fx:

`Du modtager denne e-mail, fordi du er tilmeldt nyheder om OS2ai eller registreret som kontaktperson for OS2ai.`

### 5. Footer – link til hjemmesiden

Find linket ved teksten *Gå til os2.eu*:

`href="https://www.os2.eu/"`

Ret adressen til produktets eller projektets hjemmeside, fx:

`href="https://www.os2.eu/os2ai"`

**Ret kun adressen mellem anførselstegnene.**

### 6. Footer – hjemmesidens navn

Find:

`Gå til os2.eu`

Ret til fx:

`Gå til os2.eu/os2ai`

## Trin 3: Det må du IKKE ændre

Følgende er allerede indbygget i grundskabelonen og skal bevares:

- Flettefelterne, fx `{member.update}` og `{member.unsubscribe}`
- `{content}`, som gør det muligt at bygge nyhedsbrevet i editoren
- Linket til OS2's privatlivspolitik
- Linket **Opdater lokal kontaktperson**
- Skabelonens øvrige HTML og CSS

## Trin 4: Gem og kontrollér

1. Gem skabelonen.
2. Åbn **Preview**, og kontrollér, at produktnavn og links ser rigtige ud.
3. Opret en testkampagne med produktets liste og den nye skabelon.
4. Send en testmail, og kontrollér indhold, udseende og links.

**Husk:** Afmelding og opdatering af kontaktoplysninger skal fungere korrekt, inden skabelonen bruges til en almindelig udsendelse.

## Fejlfinding: Afmelding og opdatering

Hvis links til afmelding eller opdatering af kontaktoplysninger ikke virker:

1. **Tjek flettefelterne.** Er der brugt de korrekte flettefelter frem for almindelige URL'er?
2. **Tjek listens formularer.** Er der oprettet både en afmeldingsformular og en opdateringsformular?
3. **Tjek testmetoden.** Personlige links bliver ikke altid genereret korrekt i testmails. Det betyder ikke nødvendigvis, at der er fejl i skabelonen.

Hvis du fortsat er i tvivl om, hvorvidt linksene fungerer i en rigtig udsendelse, skal problemet afklares, inden nyhedsbrevet sendes til modtagerlisten.

## Ansvar og hjælp

Produktforvaltningen har ansvar for at tage initiativ, når der er behov for ændringer i skabelonen.

OS2-sekretariatet kan hjælpe med teknisk opsætning, tilpasninger og fejlfinding efter aftale.

Se også [Heyloyaltys vejledning til HTML-skabeloner](https://guides.heyloyalty.com/help/tilpas-html-skabelonen/).
