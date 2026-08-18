---
title: Opsæt en tilmeldingsformular i Heyloyalty
layout: default
parent: Nyhedsbreve
nav_order: 6
has_toc: false
---

# Opsæt en tilmeldingsformular i Heyloyalty

Produktets tilmeldingsformular bruges af personer, der selv ønsker at følge produktets nyhedsbrev.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og muligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet.

> **💡 Sådan finder du formularen**
>
> Gå til **Lister** og klik på **de tre små prikker helt ude til højre ud for den relevante liste**.
>
> Vælg at redigere listen og gå derefter til **Formularer**.
>
> Det er ikke nok at klikke ind på selve listen.

## Grundopsætning

Giv formularen et tydeligt navn, fx:

`Tilmelding til [produktnavn]`

Brug en kort introduktion, fx:

> **Følg med i [produktnavn]**
>
> Få nyt om produktet, udviklingen og fællesskabet – og hør om arrangementer og muligheder for at være med.

Som udgangspunkt:

- brug reCAPTCHA
- undgå unødvendig specialstyling
- link til OS2's privatlivspolitik.

## Felter

Brug følgende standard:

| Felt | Obligatorisk |
|---|---|
| E-mail | Ja |
| Fornavn | Ja |
| Efternavn | Ja |
| Organisation | Nej |
| Relation til produktet | Nej |

Feltet **Relation til produktet** skal være synligt, så modtageren selv kan angive sin relation.

Brug fx følgende label på formularen:

**Hvilken relation har du til [produktnavn]? Vælg gerne flere**

Standardmuligheder:

- Bruger
- Kontaktperson
- Koordinationsgruppe
- Styregruppe
- Leverandør
- Interesseret

Relationen skal ikke automatisk sættes til `Interesseret`, fordi personer, der selv tilmelder sig, også kan have andre roller omkring produktet.

## Privatlivspolitik

Link til OS2's privatlivspolitik:

`https://www.os2.eu/privatlivspolitik`

Brug fx teksten:

`Jeg accepterer privatlivspolitikken`

## Takkeside efter formularen

Når double opt-in er aktiveret, er personen **ikke færdigtilmeldt**, når formularen er sendt.

Takkesiden skal derfor bede personen om at bekræfte tilmeldingen.

Brug fx:

> **Tak for din tilmelding.**
>
> Tjek din indbakke og bekræft din tilmelding via den mail, vi har sendt dig.

Undgå formuleringer som `Du er nu tilmeldt`, før personen har klikket på double opt-in-linket.

## Test formularen

Test formularen med en e-mailadresse, der ikke allerede står på listen.

Kontrollér:

- at obligatoriske felter fungerer
- at de valgte relationer gemmes korrekt
- at formularen viser den rigtige takkeside
- at DOI-mailen bliver sendt
- at bekræftelseslinket virker
- at kontakten står korrekt på listen efter bekræftelsen.
