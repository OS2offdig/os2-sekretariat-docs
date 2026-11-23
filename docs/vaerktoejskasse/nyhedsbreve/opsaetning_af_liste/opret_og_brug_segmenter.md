---
title: Opret og brug segmenter
layout: default
parent: Opsætning af nyhedsbrevsliste
grand_parent: Nyhedsbreve
nav_order: 20
has_children: false
has_toc: true
---

# Opret og brug segmenter
{: .no_toc }

Et segment er en gruppe modtagere, som udvælges på baggrund af oplysningerne på produktlisten.

Brug kun segmenter, hvis I har et konkret og tilbagevendende behov for at sende forskellig information til forskellige grupper.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Før du opretter et segment

Start med at formulere målgruppen helt almindeligt:

**Hvem skal have denne type mail?**

Hvis alle på produktlisten skal have mailen, skal du **ikke bruge et segment**.

Et segment er kun nødvendigt, når en bestemt del af listen skal modtage udsendelsen.

## Opret et segment

Gå til den relevante liste i Heyloyalty og vælg at oprette et nyt segment.

I segmentbuilderen vælger du det felt, du vil bruge til at udvælge modtagere.

Til målretning efter roller vil det typisk være:

`Relation til produktet`

Derefter vælger du en **operator**, som fortæller Heyloyalty, hvordan feltets værdier skal bruges.

## Vælg den rigtige operator

Når du segmenterer på **Relation til produktet**, kan du bl.a. vælge:

### Har valgt én af

Modtageren skal have **mindst én** af de valgte relationer.

Eksempel: Du vil sende til:

- Kontaktpersoner
- Koordinationsgruppen
- Styregruppen

Vælg:

`Relation til produktet` → `Har valgt én af` → `Kontaktperson`, `Koordinationsgruppe`, `Styregruppe`

Det betyder:

**Kontaktperson ELLER Koordinationsgruppe ELLER Styregruppe**

Dette vil ofte være den relevante operator, når OS2 segmenterer på relationer.

### Har valgt alle

Modtageren skal have **alle de valgte relationer samtidig**.

Hvis du vælger Kontaktperson, Koordinationsgruppe og Styregruppe, kommer kun personer med alle tre relationer med.

Det vil derfor sjældent være det, du ønsker.

### Har ikke valgt

Bruges til at udelukke personer med en bestemt relation.

Brug denne mulighed med omtanke, især fordi en person godt kan have flere relationer samtidig.

### Er tom

Finder modtagere, hvor der ikke er registreret nogen relation.

### Er ikke tom

Finder modtagere, hvor mindst én relation er registreret.

## Tjek altid resultatet

Brug funktionen til at finde **antal kontakter i det aktuelle segment**, før du gemmer eller sender.

Spørg dig selv:

**Ser antallet realistisk ud?**

Hvis ikke, så kontrollér først:

- om du har valgt det rigtige felt
- om operatoren er rigtig
- om de rigtige værdier er valgt

Forkert segmentering skyldes ofte logikken i kriterierne – ikke selve modtagerdataene.

## Brug segmentet ved udsendelse

Når du opretter en udsendelse, vælger du produktlisten og derefter det relevante segment.

Kun de modtagere, som aktuelt opfylder segmentets kriterier, bliver udvalgt.

Kontrollér altid modtagerantallet inden udsendelse.

## Du skal ikke flytte modtagere mellem segmenter

Et segment bygger på oplysningerne på kontakten.

Hvis segmentet fx består af:

`Relation til produktet = Kontaktperson`

vil en person automatisk være omfattet, når relationen Kontaktperson er registreret.

Hvis personens relation ændres, skal du derfor **opdatere kontakten – ikke segmentet**.

## Hold segmenterne enkle

Opret kun segmenter, som I faktisk har et tilbagevendende behov for.

Giv dem tydelige navne, så andre kan forstå:

- hvem segmentet indeholder
- hvad det bruges til

Hvis et segment kræver mange regler og undtagelser for at fungere, så stop op og overvej, om modtagerstrukturen kan gøres enklere.