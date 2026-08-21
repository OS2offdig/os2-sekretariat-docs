---
title: Felter og segmentering i Heyloyalty
layout: default
parent: Nyhedsbreve
nav_order: 15
has_toc: false
---
# Felter og segmentering i Heyloyalty

Når du opretter eller rydder op i en produktliste i Heyloyalty, skal felterne være så enkle som muligt.

Formålet er ikke at opbygge et CRM-system i Heyloyalty. OS2 bruger Airtable til stam- og relationsdata. Felterne i Heyloyalty skal kun gøre det muligt at vedligeholde modtagerne og målrette produktets kommunikation.

## Standardfelter på en produktliste

En produktliste skal som udgangspunkt indeholde følgende felter:

| Felt | Type | Flettefelt |
|---|---|---|
| E-mail | Standardfelt | `{member.email}` |
| Fornavn | Standardfelt | `{member.firstname}` |
| Efternavn | Standardfelt | `{member.lastname}` |
| Organisation | Tekst | `organisation` |
| Relation til produktet | Flervalgsmulighed | `produktrelation` |

### Relation til produktet

Feltet **Relation til produktet** oprettes som et felt med flere valgmuligheder.

Brug som udgangspunkt disse værdier:

- Bruger
- Kontaktperson
- Koordinationsgruppe
- Styregruppe
- Interesseret
- Leverandør

En person kan have flere relationer samtidig. En kontaktperson kan fx også være bruger eller medlem af koordinationsgruppen.

**Interesseret** bruges til personer, der følger produktet uden at have en kendt formel rolle omkring det.

## Sådan opretter du felterne

De tre standardfelter **E-mail**, **Fornavn** og **Efternavn** findes allerede i Heyloyalty og skal ikke oprettes igen.

Opret derefter:

### Organisation

- Feltnavn: `Organisation`
- Type: `Tekst`
- Flettefelt: `organisation`
- Fallback: kan stå tomt

### Relation til produktet

- Feltnavn: `Relation til produktet`
- Type: `Flervalgsmulighed`
- Flettefelt: `produktrelation`
- Fallback: kan stå tomt

Tilføj derefter de fem standardværdier: Bruger, Kontaktperson, Koordinationsgruppe, Styregruppe og Interesseret.

## Felter beskriver personer – segmenter udvælger modtagere

Opret ikke et generelt felt med navnet **Segmenter**.

Et felt skal beskrive noget om modtageren, fx:

> Relation til produktet = Kontaktperson

Et segment er derimod en gruppe af modtagere, som Heyloyalty udvælger på baggrund af felterne, fx:

> Alle modtagere, hvor Relation til produktet indeholder Kontaktperson.

Det gør det muligt at oprette og ændre segmenter senere uden at ændre de grundlæggende oplysninger om modtagerne.

## Undgå overflødige felter

Opret ikke et ekstra felt med navnet **Navn**, når Fornavn og Efternavn allerede findes som standardfelter.

Opret heller ikke ekstra felter eller relationstyper, medmindre der er et konkret og tilbagevendende behov for dem.

Målet er en enkel struktur, der kan vedligeholdes i praksis.

## Når en persons rolle ændrer sig

Hvis en person skifter rolle omkring produktet, skal feltet **Relation til produktet** opdateres.

Modtageren kan selv gøre opmærksom på ændringen, men den ansvarlige for produktets nyhedsbrevsliste har ansvar for løbende at holde oplysningerne ajour.

De autoritative stam- og relationsdata vedligeholdes i Airtable. Heyloyalty skal ikke bruges som erstatning for Airtable.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og importmuligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet. Opdager du en rettelse eller tilføjelse, så skriv endelig til kommunikation@os2.eu.
