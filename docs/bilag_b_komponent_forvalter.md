---
title: Bilag B - Rollebeskrivelser for Komponent-Ejer og Komponent-forvalter
layout: default
nav_order: 10
status: DRAFT
---

> ⚠️ **DETTE ER ET DRAFT** - Bilaget er under udarbejdelse.

# Bilag B: Detaljerede rollebeskrivelser for Komponent-Ejer og Komponent-forvalter

Dette bilag beskriver to centrale roller i OS2-fællesskabets governance-struktur for fælleskomponenter.

---

## 1. Komponent-Ejer
#### _(PRODUCT OWNER)_

### 1.1 Formål med rollen

Komponent-Ejeren er ansvarlig for komponentens strategiske retning, roadmap og kvalitet. Rollen sikrer at komponenten leverer værdi til alle anvendere og er i overensstemmelse med OS2-fællesskabets vision og mission i samabejde med arktiekturrådet.

### 1.2 Ansvarsområder

| Område | Beskrivelse |
|--------|--------------|
| **Roadmap** | Definere komponentens langsigtede udviklingsplan i samarbejde med anvenderne |
| **Strategiske beslutninger** | Godkende større ændringer og arkitekturvalg i samarbejde med arkitekturrådet |
| **Prioritering** | Prioritere features, bugs og forbedringer baseret på anvenderbehov |
| **Repræsentation** | Repræsentere komponenten overfor Arkitekturrådet |
| **Værdi-sikring** | Sikre at komponenten leverer værdi til alle anvendere |
| **Release-godkendelse** | Godkende releases før de publiceres |
| **Leverandørkoordinering** | Koordinering med leverandører omkring tekniske aftaler og aftalemæssige forhold |

### 1.3 Kompetencekrav

#### 1.3.1 Tekniske kompetencer

- Evne til at oversætte forretningsbehov til tekniske krav
- Erfaring med roadmap-planlægning og prioritering
- Forståelse for softwareudviklingsprocesser
- **Teknisk literacy:** Evne til at navigere i git-baserede værktøjer og kunne anvende og forstå standard Open Source metodikker og formater. Dette omfatter bl.a. at.
    - Kunne læse og skrive og behandle issues i projektets git baserede issue-tracker.
    - Kommunikere på skrift i simpel Markdown og håndtere opmærkning med YAML/JSON.
    - Kunne følge og forstå anmodninger om ændringer (Pull Requests - PRs).

> **Bemærk**: Dybere arkitekturforståelse kan understøttes af Arkitekturrådet og mere teknisk facilitering kan delegeres til forvalteren.

#### 1.3.2 Personlige kompetencer

- Erfaring med og forståelse for Open Source økosystemet
- Evne til at facilitere og styre diskussioner mellem interessenter
- Stærke kommunikationsevner (både tekniske og forretningsmæssige)
- Evne til at bygge bro mellem forskellige parter
- Strategisk tænkning og evne til at se helhededer

### 1.4 Tid og ressourcer

Komponent-Ejeren forventes at bruge følgende tid på rollen:

| Aktivitet | Timeforbrug |
|-----------|-------------|
| Møder, forberedelse og koordinering | min. ?? timer/måned |
| Roadmap-godkendelse og prioritering | min. ?? timer/måned |
| Teknisk facilitering (issues, PR-gennemgang) | min. 4 timer/måned |
| **Minimum** | **?? timer/måned** |

> **Bemærk**: Minimal tidsestimatet forudsætter en aktiv Komponent-forvalter og begrænsede lokale tilpasninger. Større brugerskare, hyppige upstream-opdateringer eller sikkerhedshåndtering vil kræve mere tid.

---

## 2. Komponent-forvalter (MAINTAINER)

### 2.1 Formål med rollen

Komponent-forvalteren varetager den daglige drift og vedligeholdelse af komponentens tekniske infrastruktur og processer. Rollen sikrer at komponenten er tilgængelig, opdateret og fungerer for alle anvendere.

### 2.2 Ansvarsområder

| Område | Beskrivelse |
|--------|--------------|
| **Repository management** | Vedligeholdelse af kodebasen, adgangskontroller og filstrukturer |
| **CI/CD-pipelines** | Drift og vedligeholdelse af automatiserede workflows |
| **Dokumentations tilgængelighed** | Drift af automatiserede dokumentationssites |
| **Issue-håndtering** | Triage og labeling i issue-tracker, prioritering af fejl og udviddelser sammen med PO |
| **Løbende Code review** | Koordinering af pull requests og feedback til bidragsydere |
| **Release-forberedelse** | Forberedelse og koordinering af PR-merges og releases til Komponent-Ejer |
| **Teknisk dialog** | Teknisk dialog med anvendere ved spørgsmål og problemer |


### 2.3 Krav til uafhængighed

Komponent-forvalteren må ikke repræsentere en specifik leverandørs interesser. Rollen skal være uafhængig og neutral for at sikre leverandør-neutrale fælleskomponenter.

### 2.4 Kompetencekrav

#### 2.4.1 Tekniske kompetencer

- Erfaring med versionsstyring og Git-workflows
- Forståelse for CI/CD-koncepter og pipeline-konfiguration
- Erfaring med automatisk genereret teknisk dokumentation
- Grundlæggende forståelse for sikkerhedspraksis i build / deployfaserne
- Erfaring med git baserede issue-trackers

#### 2.4.2 Personlige kompetencer

- Evne til at kommunikere tekniske emner klart
- Forståelse for effekten af genbrugelige standard løsninger, metoder og værktøjer
- Nysgerring tilgang til anvenderbehov
- Evne til at prioritere og håndtere flere opgaver
- Selvstændig og struktureret arbejdsmetode

### 2.5 Tid og ressourcer

Komponent-forvalteren forventes at bruge følgende tid på rollen:

| Aktivitet | Timeforbrug |
|-----------|-------------|
| Møder, forberedelse og admin | min. 4 timer/måned |
| Vedligeholdelse og drift |min. 15 timer/måned |
| **Total** | **19-25 timer/måned** |

> **Bemærk**: 15 timer til vedligeholdelse er vurderet som minimum for at stille faste ressourcer der kender kodebasen til rådighed. Denne domæneviden er faktoren der sætter grænsen for hvor meget vedligeholdelsesarbejde der realistisk kan håndteres, ikke mængden af arbejde.

### 2.6 Økonomisk ramme

Baseret på timepris for en staff softwarekonsulent der kender kodebasen:

- **Timepris**: 1.200-1.400 kr/time (2026)
- **Månedlig omkostning**: 19 timer × 1.200 kr = **22.800 kr/måned**
- **Årlig omkostning**: 22.800 kr × 12 = **273.600 kr/år**

> Denne pris forudsætter at konsulenten allerede kender kodebasen. Ved onboarding af ny ressourcer skal der påregnes ekstra tid til oplæring.

---

## 4. Samarbejde mellem rollerne

### 4.1 Relation mellem Komponent-Ejer og Komponent-forvalter

Komponent-Ejeren og Komponent-forvalteren arbejder tæt sammen:

- Regelmæssig koordinering om status og prioriteter
- Release-godkendelse via Komponent-Ejer
- Strategiske beslutninger træffes af Komponent-Ejer, operationelle af Komponent-forvalter

### 4.2 Relation til Arkitekturrådet

Begge roller:
- Deltager i månedlige møder ved behov
- Rapporterer om komponentens status og udfordringer
- Modtager retningslinjer fra Arkitekturrådet

### 4.3 Relation til anvendere

- **Komponent-Ejer**: Strategiske spørgsmål, roadmap, prioritering
- **Komponent-forvalter**: Tekniske dialog, fejlrapporter

---

## 5. Forventede leverancer

| Leverance | Ansvarlig | Frekvens |
|-----------|-----------|----------|
| Roadmap | Komponent-Ejer | Kvartalsvis |
| Prioriteringsliste | Komponent-Ejer | Månedlig |
| Statusrapport | Begge | Månedlig |
| Release-plan | Komponent-forvalter | Ved behov |
| Dokumentationsopdateringer | Komponent-forvalter | Ved ændringer |
| Incident-rapportering | Komponent-forvalter | Ved hændelser |


---

*Bilag til: Forslag til governance-struktur for solidarisk ejerskab og vedligehold af fælleskomponenter*