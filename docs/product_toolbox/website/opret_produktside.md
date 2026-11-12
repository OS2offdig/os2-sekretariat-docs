---
title: Opret produktside
layout: default
parent: Hjemmeside
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 10
has_children: false
has_toc: true
---

# Opret en produktside på os2.eu
{: .no_toc }

Denne guide viser, hvordan du opretter en produktside på os2.eu med OS2's fælles produktsideskabelon.

Inden du går i gang i Odoo, kan du med fordel samle produktets indhold i udfyldningsskabelonen. Den hjælper dig med at se, hvilke oplysninger der skal bruges, og hvilke dele af produktsiden der er valgfrie.

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Hent udfyldningsskabelonen

Brug udfyldningsskabelonen til at samle indholdet, inden du opretter siden i Odoo.

Du behøver ikke udfylde alle felter. Skabelonen viser, hvilke dele der er faste, valgfrie eller kun relevante i særlige tilfælde.

- **[Hent udfyldningsskabelonen som redigerbar fil]({{ '/assets/downloads/udfyldningsskabelon-til-produktside.odt' | relative_url }})**
- **[Åbn udfyldningsskabelonen i Markdown]({{ '/assets/downloads/udfyldningsskabelon-til-produktside.md' | relative_url }})**

## Opret produktsiden i Odoo

Når du har samlet indholdet i udfyldningsskabelonen, kan du oprette den nye produktside i Odoo.

### Opret en ny side fra skabelonen

1. Gå til **Hjemmeside** i Odoo.
2. Klik på **Ny** øverst til højre og vælg **Side**.
3. Vælg **Tilpasset**.
4. Vælg skabelonen **Ny produktsideskabelon_duplikér og tilpas_inkl vejledende tekst**.
5. **Afmarkér "Tilføj menu"**. Produktsiden skal ikke automatisk tilføjes som et selvstændigt menupunkt.
6. Navngiv den nye side `os2[produktnavn]_NY`.
7. Opret siden.

Den eksisterende produktside skal blive liggende, mens du arbejder på den nye.

### Udfyld produktsiden

Brug din udfyldte udfyldningsskabelon som arbejdsgrundlag.

1. Erstat den vejledende tekst i produktsideskabelonen med produktets eget indhold.
2. Slet valgfrie sektioner, der ikke er relevante.
3. Tilføj relevante links, billeder og materialer.
4. Kontrollér, at der ikke er vejledende tekst eller placeholders tilbage.

Henvis så vidt muligt til eksisterende dokumentation, GitHub og andre relevante ressourcer frem for at kopiere det samme indhold ind på produktsiden.

Har du brug for hjælp til automatiske visninger, fx arrangementer, nyheder eller Airtable, kan du kontakte OS2-sekretariatet.

## Erstat den gamle produktside

Hvis produktet allerede har en produktside på os2.eu, skal den nye side overtage den eksisterende sides URL, når den er færdig og klar til offentliggørelse.

Hvis der ikke findes en eksisterende produktside, kan du gå direkte til afsnittet **Giv den nye side den rigtige URL**.

### 1. Flyt den gamle side

1. Gå til den eksisterende produktside.
2. Vælg **Side** og derefter **Egenskaber** under **Denne side**.
3. Ændr sidens URL til `os2[produktnavn]_gammel`.
4. Fjern eventuelt markeringen **Offentliggjort**, hvis den gamle side ikke længere skal kunne ses.

### 2. Giv den nye side den rigtige URL

1. Gå til den nye produktside.
2. Vælg **Side** og derefter **Egenskaber** under **Denne side**.
3. Ændr URL'en fra `os2[produktnavn]_NY` til `os2[produktnavn]`.
4. Vælg **OS2-produkter** som sidens parent page.
5. Offentliggør siden.

## Kontrollér den nye side

Når siden er offentliggjort:

1. Åbn produktsiden som almindelig besøgende.
2. Kontrollér, at tekst, links, billeder og automatiske visninger fungerer.
3. Gå til [OS2 IT-løsninger](https://www.os2.eu/os2-it-loesninger).
4. Kontrollér, at produktet stadig linker til den rigtige produktside.

Hvis noget ikke fungerer efter skiftet, så kontakt OS2-sekretariatet.

