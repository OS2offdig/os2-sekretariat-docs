---
title: "Skriv i håndbogen"
layout: default
parent: "Værktøjskasse til projekter og produkter"
nav_order: 70
has_toc: true
---

# Skriv i håndbogen
{: .no_toc }

Alle kan bidrage til OS2-håndbogen med dokumentation, rettelser og forbedringer. Her er de vigtigste retningslinjer for placering, opbygning og godkendelse af indhold.

## Indhold
{: .no_toc .text-delta }

1. TOC
{:toc}

## Find den rette placering

Undersøg først, om indholdet allerede findes. **Placér indhold efter, hvem der skal bruge det, og hvad de skal bruge det til** – ikke kun efter emnet eller det konkrete værktøj.

- **Sådan arbejder vi i OS2:** Overordnede principper og fælles arbejdsformer. *Hvorfor arbejder OS2 sådan?*
- **Processer og rutiner:** Faste arbejdsgange, ansvar, beslutninger og overdragelser. *Hvem gør hvad og hvornår?*
- **Kommunikation:** Fælles kommunikationspraksis, roller og kanalernes formål.
- **Værktøjskasse til projekter og produkter:** Praktiske vejledninger, tjeklister og skabeloner. *Hvordan udfører jeg opgaven?*

Brug de øvrige eksisterende afsnit, når indholdet naturligt hører til dér, fx **Organisation og Roller** til beskrivelser af roller og mandater.

**Hvis noget overlapper:** Beskriv reglen og ansvaret ét sted. Beskriv den konkrete handling dér, hvor den, der skal udføre opgaven, leder efter hjælp.

Er du i tvivl om placeringen? Spørg kommunikationsmedarbejderen eller en relevant kollega. Opret ikke nye kategorier eller større strukturer uden aftale.

## Skriv kort og overskueligt

- **Én side, ét formål.** Del længere emner op, hvis det hjælper læseren.
- **Korte menutitler.** Brug præcise navne, som fylder mindst muligt i sidemenuen. Undgå gentagelser af fx værktøjsnavne, når sammenhængen allerede er tydelig.
- **`nav_order` i 10-spring:** 10, 20, 30 osv. Det giver plads til flere sider imellem.
- **Færrest mulige links.** Brug sidemenuen som navigation. Indsæt kun links, der hjælper læseren til fx en nødvendig vejledning, skabelon eller kilde – ikke links, som blot gentager sidemenuen.
- Brug korte afsnit, tydelige overskrifter og en synlig indholdsfortegnelse på sider med flere afsnit.

## Opret ændringen i GitHub

1. Find et relevant issue, eller opret et, hvis opgaven ikke allerede er beskrevet.
2. Opret en **branch fra `main`**.
3. Opret eller ret en Markdown-fil (`.md`). Brug YAML-skabelonen nedenfor til nye sider.
4. Commit ændringen, og opret en **pull request (PR)** til `main`. Beskriv ændringen, og henvis gerne til issue eller aftale.
5. Få PR'en gennemgået, og kontrollér siden i håndbogen efter merge.

Se den generelle [vejledning til at bidrage](https://handbook.os2.eu/CONTRIBUTING) for mere om GitHub-processen.

## Godkendelse før merge

**Er indholdet aftalt på forhånd?** Henvis til aftalen i PR'en. En relevant kollega eller maintainer gennemgår ændringen, inden den merges.

**Er indholdet ikke aftalt?** Opret stadig branch og PR, men afvent gennemgang. Tag fx sekretariatschefen i PR'en, så vedkommende kan vurdere indholdet og videredelegere godkendelsen.

**Nye eller ændrede principper, ansvar og fælles arbejdsgange merges som udgangspunkt ikke uden ledelsesmæssig godkendelse.** En PR er et forslag, ikke en godkendelse.

Hvis det er aftalt, at et **endnu ikke godkendt udkast** skal offentliggøres, indsættes håndbogens warning-snippet øverst i sidens indhold, lige efter YAML:

```markdown
{: .warning }
DRAFT VERSION - NOT AN OFFICIALLY APPROVED DOCUMENT
```

Markeringen viser, at indholdet ikke er officielt godkendt. Den erstatter ikke aftalen om at offentliggøre udkastet.

Mindre rettelser til fx sprog, formatering og links kan merges efter almindelig gennemgang.

## YAML-skabelon til nye sider

Kopiér skabelonen til en ny `.md`-fil, og tilpas titler, placering og indhold:

```markdown
---
title: "Kort menutitel"
layout: default
parent: "Værktøjskasse til projekter og produkter"
nav_order: 10
has_toc: true
---

# Sidens overskrift
{: .no_toc }

Kort introduktion til sidens formål.

## Indhold
{: .no_toc .text-delta }

1. TOC
{:toc}

## Første afsnit

Indhold...
```

- **`title`:** Kort titel i sidemenuen.
- **`parent`:** Den overordnede sides præcise titel. Tilføj `grand_parent`, hvis siden ligger endnu et niveau nede.
- **`nav_order`:** Vælg en ledig placering i 10-spring. `10` er kun et eksempel.
- **`has_toc`:** Brug `true` på indholdssider, og indsæt en synlig indholdsfortegnelse, hvis siden har flere afsnit.

Du kan også kopiere opbygningen fra en tilsvarende side i håndbogen.

## Valgfri hjælp fra AI

Du kan bruge en AI-assistent til at strukturere og forkorte et udkast. **Brug kun et værktøj og materiale, du har tilladelse til at bruge.** Undlad at dele fortrolige oplysninger eller personoplysninger uden et godkendt grundlag. Kontrollér altid oplysninger, formuleringer og forslag, inden du opretter en PR. AI kan ikke godkende eller fastlægge OS2's praksis.

**Forslag til prompt:**

```text
Jeg skriver dokumentation til OS2-håndbogen.

Hjælp mig med at omskrive mit materiale til en kort, konkret og
overskuelig håndbogsside.

Håndbogens relevante afsnit er:
- Sådan arbejder vi i OS2: principper og fælles arbejdsformer.
- Processer og rutiner: ansvar, beslutninger og faste forløb.
- Kommunikation: fælles kommunikationspraksis og kanaler.
- Værktøjskasse: vejledninger, tjeklister og skabeloner.
- Andre fagafsnit bruges, når de passer bedre til indholdet.

1. Foreslå placering ud fra, hvem der skal bruge indholdet,
   og hvad de skal bruge det til.
2. Foreslå en kort menutitel og tydelige overskrifter.
3. Skeln mellem principper, ansvar/arbejdsgange og praktiske
   trin. Undgå gentagelser og overflødige links.
4. Brug mit materiale som eneste faktagrundlag. Opfind ikke
   beslutninger, aftaler, regler eller roller. Markér usikkerhed.
5. Skriv i korte afsnit på konkret dansk.
6. Lever en færdig Markdown-side med YAML øverst og en synlig
   indholdsfortegnelse. Følg denne skabelon:

---
title: "Kort menutitel"
layout: default
parent: "Præcis titel på overordnet side"
nav_order: 10
has_toc: true
---

# Sidens overskrift
{: .no_toc }

Kort introduktion.

## Indhold
{: .no_toc .text-delta }

1. TOC
{:toc}

## Første afsnit

Indhold...

Tilpas `title` og `parent` til den valgte placering.
Tilføj `grand_parent`, hvis siden skal ligge to niveauer nede.
Udelad `parent`, hvis siden skal ligge på øverste niveau.
`nav_order` skal være i 10-spring; tallet 10 er kun et eksempel,
for den ledige plads skal kontrolleres i håndbogen.

Her er mit materiale:
[Indsæt tekst uden fortrolige oplysninger]
```
