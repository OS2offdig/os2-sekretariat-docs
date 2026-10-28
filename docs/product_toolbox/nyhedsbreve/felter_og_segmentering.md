---
title: Felter og segmentering
layout: default
parent: Opsætning af nyhedsbrevsliste
grand_parent: Nyhedsbreve
nav_order: 10
has_children: false
has_toc: true
---

# Felter og segmentering
{: .no_toc }

Felterne på en produktliste bruges til at strukturere oplysninger om modtagerne.

OS2 bruger nogle fælles felter på tværs af produktlisterne, så oplysningerne ligger nogenlunde ens. Det gør det muligt senere at finde eller udvælge bestemte grupper af modtagere, hvis der bliver behov for det.

Heyloyalty er ikke OS2's CRM. Stam- og relationsdata vedligeholdes i Airtable.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Hvorfor bruger vi fælles felter?

Det vigtigste er, at vi **strukturerer oplysningerne klogt fra starten**.

Hvis fx en persons relation til produktet registreres i et fast felt, kan oplysningerne senere bruges til at finde eller udvælge bestemte modtagere.

Det betyder ikke, at du normalt skal arbejde med segmentering. For de fleste produktnyhedsbreve er det både enklere og tilstrækkeligt at sende til hele produktlisten.

> **Mangler du oplysninger om nogle modtagere?**
>
> Det skal ikke forhindre dig i at komme videre. Har du fx ikke organisation eller relation på alle personer, kan du stadig oprette eller importere dem. Oplysningerne kan suppleres senere.

## Standardfelter på en produktliste

OS2 bruger som udgangspunkt disse felter:

| Felt | Type | Flettefelt |
|---|---|---|
| E-mail | Heyloyalty-standardfelt | `{member.email}` |
| Fornavn | Heyloyalty-standardfelt | `{member.firstname}` |
| Efternavn | Heyloyalty-standardfelt | `{member.lastname}` |
| Organisation | Tillægsfelt – tekst | `organisation` |
| Relation til produktet | Tillægsfelt – flervalg | `produktrelation` |

**E-mail, Fornavn og Efternavn** findes allerede i Heyloyalty.

**Organisation** og **Relation til produktet** er OS2's fælles tillægsfelter. Hvis de ikke allerede findes på produktlisten, skal de tilføjes.

## Hvis tillægsfelterne mangler

Når du redigerer produktlisten, kan du tilføje de manglende felter under **Tilføj felter**.

Opret dem sådan:

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

Brug disse standardværdier:

- Bruger
- Kontaktperson
- Koordinationsgruppe
- Styregruppe
- Leverandør
- Interesseret

En person kan have flere relationer samtidig. En kontaktperson kan fx også være bruger eller medlem af koordinationsgruppen.

**Interesseret** bruges til personer, der følger produktet uden at have en kendt formel rolle omkring det.

### Kan du ikke finde listeindstillingerne?

Du skal **ikke klikke ind på selve listen**.

**Lister → ⋮ helt ude til højre ved listen → Rediger liste**

Her finder du bl.a. felter, formularer og double opt-in.
{: .highlight }

## Felterne behøver ikke være udfyldt på alle

Standardfelterne beskriver, **hvordan vi gemmer oplysninger, når vi har dem**. De er ikke en tjekliste, som skal være komplet for hver modtager.

Hvis du fx skal importere en liste og kun har navn og e-mail på nogle personer, så importér de oplysninger, du har.

Det er bedre at få relevante modtagere på listen end at lade manglende ekstra oplysninger blive en flaskehals.

## Felter og segmentering er ikke det samme

Et **felt** beskriver noget om modtageren, fx:

> Relation til produktet = Kontaktperson

Et **segment** er en gruppe, der kan udvælges på baggrund af oplysningerne i felterne, fx alle modtagere med relationen Kontaktperson.

Det er derfor, vi bruger faste felter: **så muligheden findes senere, hvis der bliver brug for den.**

Du behøver som udgangspunkt ikke oprette segmenter for at bruge produktets nyhedsbrev.

## Undgå overflødige felter

Opret ikke et ekstra felt med navnet **Navn**, når Fornavn og Efternavn allerede findes.

Opret heller ikke nye felter eller relationstyper, medmindre der er et konkret og tilbagevendende behov.

Målet er en enkel struktur, der kan vedligeholdes i praksis.

## Når oplysninger ændrer sig

Hvis en persons rolle omkring produktet ændrer sig, bør **Relation til produktet** opdateres.

De autoritative stam- og relationsdata vedligeholdes i Airtable. Heyloyalty indeholder kun de oplysninger, der er nyttige i forbindelse med produktets nyhedsbrev og kommunikation.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og muligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet. Opdager du en rettelse eller tilføjelse, så skriv endelig til kommunikation@os2.eu.
