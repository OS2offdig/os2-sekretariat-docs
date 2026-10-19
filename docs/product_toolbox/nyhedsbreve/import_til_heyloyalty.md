---
title: Importér modtagere
layout: default
parent: Nyhedsbreve
nav_order: 80
has_children: false
has_toc: true
---

# Importér modtagere
{: .no_toc }

Brug denne guide, når du skal tilføje flere modtagere til produktets nyhedsbrevsliste på én gang.

Skal du kun tilføje én person, bruger du **Opret én modtager**.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Find din modtagerliste

Du har ofte allerede de relevante personer samlet i et Excel-ark eller en anden liste.

Hvis du ikke har en opdateret liste, kan du spørge OS2-sekretariatet, om de kan hjælpe med at eksportere de relevante oplysninger fra Airtable.

Det kan især være nyttigt første gang, en produktliste skal opdateres eller bringes ajour.

> **Airtable er OS2's system til stam- og relationsdata.**
>
> Heyloyalty bruges til udsendelse og målretning af nyhedsbreve og skal ikke fungere som CRM-system.

## Før du importerer

Kontrollér, at produktlisten har OS2's fælles felter:

- E-mail
- Fornavn
- Efternavn
- Organisation
- Relation til produktet

Hvis **Organisation** eller **Relation til produktet** ikke allerede findes på listen, skal de oprettes som tillægsfelter. Se **Felter og segmentering**.

Du behøver ikke have alle oplysninger om alle modtagere for at importere dem.

Mangler du fx organisation eller relation på nogle personer, skal det **ikke være en flaskehals**. Importér de oplysninger, du har. Resten kan suppleres senere.

## Klargør filen

Heyloyalty importerer fra en CSV-fil.

Hvis din modtagerliste ligger i Excel eller et andet regneark, skal du derfor gemme eller eksportere en kopi som **CSV UTF-8**.

Brug som udgangspunkt disse kolonner:

| email | fornavn | efternavn | organisation | produktrelation |
|---|---|---|---|---|

Eksempel:

| email | fornavn | efternavn | organisation | produktrelation |
|---|---|---|---|---|
| anna@example.dk | Anna | Jensen | Aarhus Kommune | Kontaktperson |
| bo@example.dk | Bo | Hansen | Favrskov Kommune | Bruger\|Koordinationsgruppe |

Hvis en person har flere relationer, adskilles værdierne med en lodret streg (`|`).

Værdierne i `produktrelation` skal svare til de valgmuligheder, der findes i Heyloyalty:

- Bruger
- Kontaktperson
- Koordinationsgruppe
- Styregruppe
- Leverandør
- Interesseret

Det er ikke teknisk nødvendigt, at kolonnerne har præcis de viste navne. Kolonnerne matches med Heyloyaltys felter under importen.

De fælles navne gør det dog lettere at gennemskue filen og fejlfinde senere.

### Hent en skabelon til klargøring af csv.-filen her. 

Følg vejledningen i dokumentet.

Download ved at klikke: [Skabelon til import af kontakter](/assets/downloads/OS2_skabelon_import_kontakter_Heyloyalty.ods) .ods

Download ved at klikke: [Skabelon til import af kontakter](/assets/downloads/OS2_skabelon_import_kontakter_Heyloyalty.xlsx) .xlsx

## Sådan importerer du

1. Gå til **Lister**.
2. Klik ind på den relevante produktliste.
3. Vælg **Import/Eksport → Importer medlemmer**.
4. Vælg din CSV-fil.
5. Vælg importtype.

Ved almindelig vedligeholdelse af en produktliste vil **Opret eller opdater kontakter** typisk være det relevante valg:

- eksisterende kontakter opdateres
- nye kontakter oprettes.

Brug **e-mail** som identifikation af kontakten.

6. Vælg den delimiter, CSV-filen bruger, typisk semikolon.
7. Angiv, at filen indeholder kolonneoverskrifter.
8. Match kolonnerne i filen med de relevante felter i Heyloyalty, fx:

   - `email` → E-mail
   - `fornavn` → Fornavn
   - `efternavn` → Efternavn
   - `organisation` → Organisation
   - `produktrelation` → Relation til produktet

9. Gennemgå indstillingerne for double opt-in, tidligere afmeldte modtagere og automations.
10. Kontrollér feltmatchningen én gang til.
11. Gennemfør importen.

## Hvis du importerer rollebaserede modtagere

Double opt-in bruges som udgangspunkt ved **frivillig selvtilmelding**.

Hvis du derimod importerer personer, fordi de har en relevant rolle omkring produktet – fx kontaktpersoner eller medlemmer af styre- og koordinationsgruppen – kan de importeres uden double opt-in.

Vælg derfor under importen, at kontakterne oprettes **uden double opt-in-bekræftelsesmail**, når det er en rollebaseret liste.

Hvis Heyloyalty også giver mulighed for at fravælge en velkomst-trigger-mail, skal du kontrollere, om den er relevant for den konkrete import.

> **Husk forskellen**
>
> Det afgørende er ikke, om kontakten oprettes manuelt eller via import. Det afgørende er **hvorfor personen kommer på listen**.
>
> Frivillig selvtilmelding følger double opt-in-flowet. Rollebaseret registrering kan ske uden double opt-in.

## Vigtigt om tidligere afmeldte

En import må ikke bruges til utilsigtet at genaktivere personer, der tidligere har afmeldt sig nyhedsbrevet.

Kontrollér derfor altid indstillingen for tidligere afmeldte modtagere, inden importen gennemføres.

## Når importen er færdig

Kontrollér et par af de importerede kontakter:

- Er de kommet på den rigtige liste?
- Er navn og e-mail placeret korrekt?
- Er Organisation kommet med, hvis oplysningerne fandtes?
- Er Relation til produktet registreret korrekt?
- Er personer med flere relationer blevet importeret som forventet?

Du behøver ikke udfylde alle manglende oplysninger med det samme. Formålet er først og fremmest at få de relevante modtagere korrekt ind på listen.

## Hvis importen ikke virker

Tjek først:

- **Er filen gemt som CSV UTF-8?**
- **Er delimiter valgt korrekt?** Hvis alle oplysninger ser ud til at ligge i én kolonne, er delimiteren sandsynligvis forkert.
- **Har du angivet, at filen indeholder kolonneoverskrifter?**
- **Er e-mail mappet til feltet E-mail?**
- **Er `produktrelation` mappet til Relation til produktet?**
- **Findes værdierne i `produktrelation` som valgmuligheder i Heyloyalty?**
- **Er værdierne stavet præcist som i Heyloyalty?**
- **Har en person flere relationer?** Brug `|` mellem værdierne, fx `Bruger|Kontaktperson`.
- **Er der dubletter af samme e-mail i CSV-filen?**
- **Er e-mailadresserne gyldige?**
- **Forsøger du at importere en tidligere afmeldt modtager?**

Hvis Heyloyalty afviser enkelte rækker, kan systemet danne en `import_errors.csv` med oplysninger om de kontakter, der ikke kunne importeres. Brug den til at finde og rette fejlene.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og importmuligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet.
