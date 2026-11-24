---
title: Sådan bidrager du
layout: default
nav_exclude: true
nav_order: 99
---

# Sådan bidrager du til OS2-håndbogen

Tak fordi du vil bidrage til OS2-håndbogen!

Håndbogen vedligeholdes løbende, så produkt- og projektfællesskaber, sekretariatet og andre involverede kan finde opdateret og brugbar dokumentation.

Vi arbejder efter tilgangen *Docs as Code*: Dokumentationen skrives i Markdown, og ændringer håndteres åbent gennem GitHub.

## Kom i gang

### 1. Find eller opret et issue

Undersøg først, om der allerede findes et issue om den ændring, du vil foreslå.

Hvis ikke, så opret et issue i repositoryet, og beskriv kort:
- Hvad der skal ændres eller tilføjes
- Hvorfor ændringen er nødvendig
- Hvornår opgaven kan betragtes som færdig

### 2. Opret en branch og lav dine ændringer

- Opret en branch fra `main`.
- Redigér eller opret de relevante Markdown-filer.
- Gem ændringerne med en beskrivende commit-besked.
- Opret en pull request (PR), når ændringerne er klar, og henvis til det relevante issue.

### 3. Få ændringerne gennemgået

En kollega eller maintainer gennemgår din pull request. Når ændringerne er godkendt og flettet ind i `main`, bliver håndbogen opdateret.

## Når du skriver dokumentation

**Tag udgangspunkt i brugerens behov.**

- Placér indhold efter, hvem der skal bruge det, og hvad de skal bruge det til.
- Brug den eksisterende struktur frem for at oprette nye kategorier.
- Giv hver side ét tydeligt formål og en beskrivende titel.
- Skriv kort, konkret og i aktiv form.
- Skeln mellem gældende praksis, besluttede krav og forslag, der endnu ikke er vedtaget.
- Undgå at gentage regler og vejledninger, der allerede er beskrevet andre steder.

Læs også [README.md](README.md) om håndbogens formål og principper for organisering af indhold.

## Struktur og navigation

Når du opretter en ny side:

- Brug Markdown (`.md`) og korrekt YAML-frontmatter.
- Følg den eksisterende navigation med `parent`, eventuelt `grand_parent` og `nav_order`.
- Brug som udgangspunkt spring på 10 i `nav_order`, så der er plads til nye sider.
- Kontrollér, at siden vises det rigtige sted i navigationen.

Den praktiske vejledning findes i håndbogens værktøjskasse under **Skriv i håndbogen**.

## Samarbejde og vedligeholdelse

- Vær konstruktiv og respektfuld i issues og pull requests.
- Forklar gerne, hvorfor du foreslår en ændring.
- Ret forældet eller misvisende information, når du opdager den.
- Er du i tvivl om indhold eller placering, så brug et issue til at få det afklaret.

## Hjælp og spørgsmål

Har du spørgsmål eller forslag, kan du oprette et issue eller kontakte OS2-sekretariatet på [os2@os2.eu](mailto:os2@os2.eu).
