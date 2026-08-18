---
title: Importér modtagere
layout: default
parent: Nyhedsbreve
nav_order: 30
has_toc: false
---
# Importér modtagere til Heyloyalty

Modtagere kan komme på en produktliste i Heyloyalty på to måder:

1. **De tilmelder sig selv**, fx via en tilmeldingsformular.
2. **De importeres manuelt**, fx når kontaktpersoner eller medlemmer af styre- og koordinationsgrupper skal registreres på baggrund af oplysninger fra Airtable.

Denne guide beskriver manuel import.

> Airtable er OS2's system til stam- og relationsdata. Heyloyalty bruges til udsendelse og målretning af nyhedsbreve og skal ikke fungere som CRM-system.

## Før du importerer

Kontrollér først, at produktlisten har de fælles standardfelter:

- E-mail
- Fornavn
- Efternavn
- Organisation
- Relation til produktet

Feltet **Relation til produktet** skal være et flervalgsfelt med disse standardværdier:

- Bruger
- Kontaktperson
- Koordinationsgruppe
- Styregruppe
- Interesseret

En person kan have flere relationer samtidig.

## Klargør CSV-filen

Gem filen som **CSV UTF-8**.

Brug som udgangspunkt disse kolonner:

| email | fornavn | efternavn | organisation | produktrelation |
|---|---|---|---|---|

Eksempel:

| email | fornavn | efternavn | organisation | produktrelation |
|---|---|---|---|---|
| anna@example.dk | Anna | Jensen | Aarhus Kommune | Kontaktperson |
| bo@example.dk | Bo | Hansen | Favrskov Kommune | Bruger\|Koordinationsgruppe |

Hvis en person har flere relationer, adskilles værdierne med en lodret streg (`|`).

Værdierne i `produktrelation` skal være stavet præcis som valgmulighederne i Heyloyalty.

Det er ikke teknisk nødvendigt, at CSV-kolonnerne har præcis disse navne, fordi kolonnerne matches med Heyloyaltys felter under importen. Vi bruger alligevel de samme standardnavne for at gøre import og fejlfinding lettere.

## Sådan importerer du

1. Gå til **Lister** i Heyloyalty.
2. Vælg den relevante produktliste.
3. Vælg **Import/Eksport → Importer medlemmer**.
4. Vælg CSV-filen.
5. Vælg importtype.

Ved almindelig vedligeholdelse af en produktliste vil **Opret eller opdater kontakter** typisk være det relevante valg:

- eksisterende kontakter opdateres
- nye kontakter oprettes.

Brug **e-mail** som identifikation af kontakten.

6. Vælg den delimiter, CSV-filen bruger, typisk semikolon.
7. Angiv, at filen har kolonneoverskrifter.
8. Match hver CSV-kolonne med det tilsvarende felt i Heyloyalty:

   - `email` → E-mail
   - `fornavn` → Fornavn
   - `efternavn` → Efternavn
   - `organisation` → Organisation
   - `produktrelation` → Relation til produktet

9. Gennemgå indstillingerne for tidligere afmeldte modtagere og automations.
10. Kontrollér feltmatchningen én gang til.
11. Klik **Importer medlemmer**.

## Vigtigt om tidligere afmeldte

En manuel import må ikke bruges til utilsigtet at genaktivere personer, der tidligere har afmeldt sig nyhedsbrevet.

Kontrollér derfor altid indstillingen for tidligere afmeldte modtagere, inden importen gennemføres.

## Manuel import er ikke det samme som selvtilmelding

En person, der selv tilmelder sig et produktnyhedsbrev, følger produktets tilmeldingsflow og eventuelle double opt-in.

Manuel import bruges bl.a. til at vedligeholde rollebaserede modtagere fra Airtable.

De to måder at komme på listen skal derfor ikke behandles som samme arbejdsgang.

> **OBS: Double opt-in ved manuel import**
>
> Det skal afklares, præcis hvordan Heyloyalty håndterer double opt-in, når modtagere oprettes via manuel CSV-import på en liste med double opt-in aktiveret.
>
> Heyloyalty giver ved import mulighed for at vælge, om aktive automations skal sendes til importerede kontakter, men den generelle importguide beskriver ikke entydigt, om en double opt-in-mail udløses ved manuel CSV-import.
>
> Opdatér denne guide, når praksis er afklaret.

## Hvis importen ikke virker

Tjek først:

- **Er filen gemt som CSV UTF-8?**
- **Er delimiter valgt korrekt?** Hvis alle data ser ud til at ligge i én kolonne, er delimiteren sandsynligvis forkert.
- **Har du angivet, at filen indeholder kolonneoverskrifter?**
- **Er e-mail mappet til feltet E-mail?**
- **Er `produktrelation` mappet til Relation til produktet?**
- **Findes alle værdier i `produktrelation` som valgmuligheder i Heyloyalty?**
- **Er værdierne stavet præcist som i Heyloyalty?** Fx `Koordinationsgruppe` og ikke `koordinationsgruppe`.
- **Har en person flere relationer?** Brug `|` mellem værdierne, fx `Bruger|Kontaktperson`.
- **Er der dubletter af samme e-mail i CSV-filen?**
- **Er e-mailadresserne gyldige?**
- **Forsøger du at importere en tidligere afmeldt modtager?**

Hvis Heyloyalty afviser enkelte rækker, sender systemet en `import_errors.csv` med oplysninger om de kontakter, der ikke kunne importeres. Brug den til at finde og rette fejlene.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og importmuligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet.
