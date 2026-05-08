---
title: Governance struktur for solidarisk ejerskab og vedligehold af fælleskomponenter
layout: default
nav_order: 10
status: DRAFT
---

> **DETTE ER ET DRAFT** - Dokumentet er under udarbejde og afventer review.

# Forslag til governance-struktur for fælleskomponenter i OS2-fællesskabet

## 1. Resumé og anbefaling

OS2-fællesskabet råder over 20 aktive og 7 produkter i vedligeholdelsestilstand og forventer at tilføje 7-8 nye projekter inden for de næste 1-3 år. Mange af disse projekter er afhængige af de samme grundlæggende funktioner til sikkerhed, interoperabilitet, systemintegrationer og driftsafvikling (såsom adgangsstyring, dataintegration og systemovervågning). Uden en fælles governance-struktur gentager hvert projekt arbejdet med at implementere, vedligeholde og sikre egne divergerende udgaver af disse funktioner. Dette resulterer i ineffektiv ressourceanvendelse, øgede omkostninger og fragmenteret sikkerhed.

## 2. Problem og konsekvenser

### 2.1 Udfordringer

OS2-fællesskabet står over for tre udfordringer:

1. **Begrænset transparens og genbrugelighed**: Når et projekt udvikler en komponent, forbliver den i projektets silo. Andre projekter opdager den ikke og udvikler derfor egne løsninger. Vurdering af delings og genbrugspotentiale foregår ikke i dag, da det betragtes som unødige og ikke relevante udgifter for det enkelte produkt.

2. **Manglende fælles finansieringsmodeller**: Projekterne har egne budgetter, men der er ingen mekanisme til at finansiere tilpasning og vedligehold af genbrugelige komponenter der kan betjene flere produkter eller projekter.

3. **Fraværet af uafhængige tekniske forvalter-roller**: Projekter overlader oftest praktiskt ejerskab og vedligehold til udviklingsleverndøren. Dette modvirker oftest gebrug og solidarisk vedligehold, da det sjældent matcher leverandørens forretningsmodel.

### 2.2 Konsekvenser

- Forhøjede omkostninger ved at genopfinde løsninger
- Sikkerhedsrisici fra fragmenteret vedligeholdelse
- Hindret vidensdeling mellem projekter
- Opbygning af teknisk gæld i hvert projekt
- Utidssvarende løsninger der hurtigt bliver forældede
- Utilsigtet leverandørbinding til mange forskellige leverandører
- Rekrutteringsudfordringer pga. lokale, projektspecifikke løsninger

## 3. Anbefalede organisatoriske roller

### 3.1 Arkitekturråd

**Hvad**: Et strategisk organ med ansvar for at fastsætte standarder for fælleskomponenter, godkende nye komponenter, og prioritere ressourceanvendelse.

**Medlemmer**: Erfarne tekniske repræsentanter fra forskellige projekter samt eventuelt eksterne faglige sparringspartnere.

**Mødefrekvens**: Månedligt.

> Detaljeret kommissorium: Bilag A. (skal udarbejdes)

### 3.2 Komponent-Ejer
_(PRODUCT OWNER)_

**Hvert komponent har en Komponent-Ejer der er ansvarlig for komponentens strategiske retning, roadmap og kvalitet.** Komponent-Ejeren behøver ikke at være en person på fuld tid, men skal have dedikeret tid afsat til rollen. Vedkommende er ansvarlig for at:

- Definere komponentens roadmap i samarbejde med brugerne
- Godkende større ændringer og arkitekturvalg
- Repræsentere komponenten overfor Arkitekturrådet
- Sikre at komponenten leverer værdi til alle anvendere

### 3.3 Teknisk Komponent-forvalter 
_(MAINTAINER)_

**Hver komponent har en Komponent-forvalter der varetager den daglige drift og vedligeholdelse af komponentens infrastruktur og processer. forvalteren er Komponent ejerens forlængede tekniske arm ned i projektet**

Dette inkluderer:
- Repository management og adgangskontrol
- Vedligeholdelse af CI/CD-pipelines i repoet
- Drift af automatisering bag genererede dokumentationssites.
- Triaging, labeling og styring af issue-trackeren
- Koordinering af pull requests og feedback til komponent anvendere

**Krav til uafhængighed**: Komponent-forvalteren må ikke repræsentere en specifik leverandørs interesser. Rollen skal være uafhængig og neutral for at sikre leverandør-neutrale fælleskomponenter.

> Detaljerede rollebeskrivelser og kompetencekrav for begge roller: [Bilag B](bilag_b_komponent_forvalter.md).

> **Vigtig bemærkning om rollekompetencer**: Begge roller kræver betydelig teknisk kompetence, men af forskellig art:
> - **Komponent-Ejer** kræver arkitekturforståelse, roadmap-planlægning og evne til at oversætte anvenderbehov til tekniske krav
> - **Komponent-forvalter** kræver praktisk erfaring med GitOps, CI/CD-pipelines, repository management og release-processer
> 
> I offentlig sektor er det sjældent at finde enkeltpersoner der mestrer begge sæt kompetencer på højt niveau. Derfor anbefales det stærkt at:
> 1. Enten dele rollerne mellem to personer med komplementære kompetencer
> 2. Eller sikre at den enkelte person har adgang til teknisk støtte (f.eks. fra en ekstern konsulent eller en teknisk ekspert i Arkitekturrådet) for de områder hvor vedkommende ikke er ekspert
> 
> At undervurdere tekniske krav til enten rolle risikerer at føre til dårlig vedligeholdelse, fragil infrastruktur og manglende evne til at koordinere effektivt med anvendere og leverandører.

## 4. Finansiering

### 4.1 Fælles betalingsmodeller for fælleskomponenter

Baseret på research af eksisterende modeller fra open source-fællesskaber og offentlige konsortier foreslåes tre modeller der vurderes som de mest retfærdige og gennemsigtige:

**Model 1: Udvidelse af fællesbidraget**
- En andel af det eksisterende 9% fællesbidrag øremærkes til fælleskomponenter
- Alle medlemskommuner bidrager obligatorisk via deres eksisterende medlemsbidrag
- Pengene samles i en fælles pulje der kan bruges på tværs af alle fælleskomponenter
- Forvaltes af Arkitekturråd med transparens omkring anvendelse
- Fordel: Simpel model der ikke kræver nye aftaler eller administrativ kompleksitet
- Ulempe: Kan opleves som "usynlig skat" uden direkte synlighed for bidragydere

**Model 2: Headcount-baseret bidrag**
- Medlemskommuner bidrager til fælleskomponenterne baseret på antal borgere/indbyggere
- Større kommuner bidrager mere, mindre kommuner bidrager mindre
- Fordel: Progressiv og retfærdig model der afspejler betalingsevne og nytte
- Ulempe: Kræver enighed om fordelingsnøgle og årlig opdatering

**Model 3: Komponent-specifik konsortium-pulje**
- For hver komponent dannes en pulje af interesserede projekter
- Kun projekter der bruger komponenten bidrager til den - ikke alle medlemmer
- Pengene går specifikt til den ene komponent, ikke til en fælles pulje
- Deltagerne betaler et fast årligt beløb og får til gengæld indflydelse på prioritering
- Fordel: Forbrugsbaseret model - kun anvendere betaler for komponenten
- Ulempe: Kan skabe ulige adgang og fragmentering mellem komponenter

**Model 4: Foreningsfond (inspireret af OSS-fonde som .NET Foundation, Apereo)**
- En dedikeret fond etableret under foreningen med eget regnskab og formål
- Finansieres via frivillige bidrag fra medlemmer, virksomhedssponsorer og/eller eksterne fondsmidler
- Kan søge eksterne bevillinger fra private fonde, EU-programmer mv.
- Fokus på langsigtet vedligeholdelse af kritisk open source-infrastruktur
- Kan finansiere både drift af egne skabeloner OG upstream-bidrag til FOSS-projekter
- Eksempler: .NET Foundation (sponsor + medlemskab), Apereo (grant + medlemskab)
- Fordel: Sikrer langsigtet, stabil finansiering med professionel forvaltning
- Ulempe: Kræver aktiv rekruttering af bidragydere og fondsmidler

> Detaljeret analyse af modellerne med beregningseksempler: Se bilag C.

**Anbefaling**: Start med Model 1 (udvidelse af fællesbidraget) for pilotfasen og evaluer om Model 2, 3 eller 4 giver mere retfærdig fordeling ved bredere udrulning.

## 5. Pilot: OS2Adgang-komponenten

### 5.1 Baggrund

Os2Adgang er en tilpasning og udviddelse af KeyCloak der er en open source-løsning til identitets- og adgangsstyring. OS2ai har allerede investeret i en implementering, men andre projekter har ikke adgang til denne investering, på trods af at flere er afhængige af leverandør-leverede løsninger der baserer sig på samme komponent, blot i egne implemeteringsudgaver. Det er derfor et oplagt pilot-projekt.

### 5.2 Formål

Pilotens formål er at demonstrere at governance-strukturen fungerer i praksis og dokumentere erfaringerne.

### 5.3 Tidsplan og milepæle

Piloten forventes at strække sig over 6 måneder med tre faser: etablering, onboarding og evaluering.

> Detaljeret tidsplan og milepæle: Se bilag D.

### 5.4 Succeskriterier

- Komponenten anvendes af minimum 2 andre projekter ud over originalprojektet
- Komponent-forvalter-rollen har fungeret med acceptable responstider
- Dokumenteret læring til bredere udrulning

## 6. Bilag (referencer)

Dokumentet understøttes af følgende bilag med detaljerede "hvordan"-beskrivelser:

- **Bilag A**: Kommissorium for Arkitekturråd (mødestruktur, kommissorium, medlemskriterier)
- **Bilag B**: Detaljerede rollebeskrivelser for Komponent-Ejer og Komponent-forvalter (kompetencekrav, ansvarsområder, timeforbrug, økonomi)
- **Bilag C**: Detaljeret finansieringsmodel og skaleringsformel
- **Bilag D**: Detaljeret implementeringsplan for pilot
- **Bilag E**: Teknisk referencearkitektur for declarative konfiguration og adoption

---

*Dokumentet er udarbejdet som beslutningsindstilling for OS2-bestyrelsen.*

> **Status**: DRAFT - Afventer review og godkendelse