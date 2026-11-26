---
title: Organisationsdiagram
layout: default
parent: Organisation og roller
nav_order: 40
has_toc: true
---

# Organisationsdiagram
{: .no_toc }

## Indholdsfortegnelse
{: .no_toc .text-delta }

1. TOC
{:toc}

## Organisering og ansvar

OS2 er organiseret som en forening med en generalforsamling, bestyrelse og et sekretariat. 

De enkelte OS2-produkter har deres egen organisering inden for OS2's fælles rammer. OS2-projekter kan være organiseret forskelligt afhængigt af projektets formål og udviklingsfase.

Diagrammet viser derfor den overordnede organisering og den typiske struktur omkring et OS2-produkt.

Medlemskab af foreningen og tilslutning til et bestemt produkt er to forskellige forhold.

```mermaid
flowchart TD
    M["Foreningens medlemmer"] -->|deltager i| GF["Generalforsamling"]
    GF -->|vælger| B["Bestyrelse"]
    B -->|fastlægger rammer for| S["OS2-sekretariatet"]

B -->|fastlægger fælles rammer| P["OS2-produkt"]
B -->|fastlægger fælles rammer| PR["OS2-projekt"]
PR --> PO["Organisering tilpasses det enkelte projekt"]

    T["Tilsluttede myndigheder"] -->|tilslutning| P

    P --- SG["Produktets styregruppe"]
    SG -->|fastlægger mandat| KG["Koordinationsgruppe"]
    SG -->|fastlægger mandat| PF["Produktforvaltning"]
    classDef forening fill:#E6F0FA,stroke:#3976A3,color:#17334A,font-size:18px;
classDef sekretariat fill:#DDF2E5,stroke:#2D7951,color:#153D2A,font-size:18px;
classDef produkt fill:#FFF0CF,stroke:#B87C27,color:#5B401D,font-size:18px;
classDef projekt fill:#EEE9F9,stroke:#715FA8,color:#36275A,font-size:18px;
classDef myndighed fill:#F0F0F0,stroke:#5C6470,color:#303740,font-size:18px;

class M,GF,B forening;
class S sekretariat;
class P,SG,KG,PF produkt;
class PR,PO projekt;
class T myndighed;
```

## OS2 som fællesskab

OS2 er mere end en formel organisation. Fællesskabet bygger på samarbejde mellem offentlige myndigheder, produkt- og projektfællesskaber, leverandører og andre bidragydere.

Samarbejdet skaber mulighed for at dele viden, erfaringer og ressourcer – og udvikle og forvalte digitale løsninger i fællesskab.

Diagrammet illustrerer de forskellige dele af OS2-fællesskabet og deres bidrag. Det viser ikke formelle ledelses- eller ansvarsforhold.

```mermaid
mindmap
  root((OS2-fællesskabet))
    Foreningen
      Medlemmer
      Bestyrelse
    Projekter og produkter
      Styregrupper
      Koordinationsgrupper
      Produktforvaltning
    Myndigheder
      Tilsluttede myndigheder
      Fagpersoner og lokale kontaktpersoner
    Faglige fællesskaber
      Faggrupper
      Netværk og videndeling
    Andre bidragydere
      Leverandører
      Samarbejdspartnere
    Sekretariatet
      Rådgivning og koordinering
      Fælles værktøjer og rammer
```