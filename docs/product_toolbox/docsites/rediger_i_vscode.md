---
title: Rediger i VS Code
layout: default
parent: Doc-sites
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 10
has_children: false
has_toc: true
---

# Rediger i VS Code

{: .no_toc }

Denne guide viser, hvordan du redigerer dokumentationssider i **Visual Studio Code (VS Code)** og deler ændringer via **GitHub**. Du behøver ikke kunne programmere.

Guiden bruger OS2-håndbogen som eksempel, men fremgangsmåden kan også bruges til andre doc-sites, der ligger på GitHub. Kontrollér altid det pågældende sites egne regler og godkendelsesproces.

**Kort fortalt:** Skriv og gem i VS Code → commit og send til GitHub → opret pull request og merge i browseren.

## Indhold

{: .no_toc .text-delta }

1. TOC
  {:toc}

## Første gang: Gør computeren klar

Disse trin skal kun udføres første gang på en ny computer.

### 1. Installer VS Code og Git

1. Installer **Visual Studio Code**.
2. Åbn VS Code, og klik på **Source Control** (ikonet med forgrenede linjer i venstre side).
3. Hvis VS Code fortæller, at **Git** mangler, skal det også installeres:
  - **Windows:** Installer *Git for Windows*. Standardindstillingerne er normalt tilstrækkelige.
  - **Mac:** Hvis macOS tilbyder at installere *Command Line Tools*, kan du acceptere det.
4. Luk og åbn VS Code igen, eller klik på **Reload**, hvis programmet tilbyder det.

**Git** er det værktøj, der holder styr på ændringer i filer. Du behøver ikke bruge Terminal til den almindelige arbejdsgang i denne guide.

### 2. Hent dokumentationen fra GitHub (Clone)

1. Åbn **Welcome** i VS Code. Hvis den ikke er synlig, vælg **Help → Welcome** i den øverste menulinje.
  
2. Klik på **Clone Git Repository…**.
  
3. Indsæt GitHub-adressen til det repository, du skal arbejde i. For OS2-håndbogen er adressen:
  
  `https://github.com/OS2offdig/os2-sekretariat-docs.git`
  
4. Vælg en mappe **på din egen computer**, fx `GitHub` i en lokal dokumentmappe. Undgå mapper, der synkroniseres med Nextcloud, OneDrive eller iCloud.
  
5. Klik på **Select as Repository Destination** og derefter **Open**, når VS Code spørger.
  
6. Godkend **Trust**, hvis du genkender repositoryet som et, du skal arbejde i.
  

**Clone** betyder, at VS Code henter en kopi af filerne ned på computeren. Den fælles version ligger fortsat på GitHub. Du skal ikke downloade filerne én ad gangen.

### 3. Find de vigtigste steder i VS Code

- **Explorer** (fil-/dokumentikon i venstre side): Her åbner du filer og mapper.
- **Source Control** (ikonet med forgrenede linjer): Her gennemser og committer du ændringer.
- **Branchnavnet nederst til venstre:** Her skifter eller opretter du en branch.
- **File → Open Folder…:** Åbn en mappe, du allerede har hentet til computeren.
- **File → Close Folder** eller **Close Workspace:** Luk det åbne arbejdsområde uden at slette filer.

Knappernes farver kan se forskellige ud afhængigt af dit tema og din computer. Gå efter **navne og placering**, ikke farver.

## Start en ny opgave

En **branch** er en separat arbejdsudgave, hvor du kan ændre filer uden at ændre den fælles `main` direkte.

1. Åbn det rigtige repository i VS Code.
2. Klik på branchnavnet **nederst til venstre**, og vælg **main**.
3. Åbn **Source Control**. Klik på **Sync Changes**, hvis knappen vises, eller vælg **… → Pull** i Source Control-menuen. Så opdateres din lokale `main`.
4. Ryd eventuelt op i åbne faner via **File → Close All Editors**.
5. Klik igen på branchnavnet nederst til venstre, og vælg **Create new branch…**.
6. Giv branchen et kort, beskrivende navn, fx `opdater-nyhedsbrev-vejledning`.

**Skal du fortsætte på en eksisterende branch?** Vælg den i branchmenuen i stedet for at oprette en ny. Kontrollér, at du står på den rigtige branch, inden du redigerer.

## Rediger og opret filer

### Ret en eksisterende side

1. Klik på **Explorer** i venstre side.
2. Fold mapperne ud, og klik på den relevante `.md`-fil.
3. Ret direkte i teksten. Du behøver ikke klikke på en redigeringsblyant som på GitHub.
4. Vælg **File → Save** eller **File → Save All**. Du kan også slå **File → Auto Save** til.

**Save gemmer kun på computeren – ikke på GitHub.**

### Opret en ny Markdown-fil

1. Højreklik på den mappe i Explorer, hvor filen skal ligge.
2. Vælg **New File…**.
3. Skriv et filnavn, der slutter på `.md`, fx `send-nyhedsbrev.md`, og tryk **Enter**.
4. Indsæt tekst og sidens nødvendige YAML-oplysninger øverst. Gem filen.

### Opret en mappe og en oversigtsside

1. Højreklik på den overordnede mappe i Explorer.
2. Vælg **New Folder…**, skriv navnet, og tryk **Enter**.
3. I OS2-håndbogen oprettes normalt en **`index.md`** i nye undermapper, så afdelingen har sin egen oversigtsside med relevant YAML.

Git registrerer ikke en helt tom mappe. Den skal indeholde mindst én fil, før den kommer med til GitHub.

### Omdøb eller flyt en fil

- **Omdøb:** Højreklik på filen i Explorer → **Rename**. Behold `.md` til sidst.
- **Flyt:** Træk filen fra den nuværende mappe til den nye mappe i Explorer.

En flytning eller omdøbning kan ændre sidens adresse. Kontrollér eventuelle links til siden.

### Forstå YAML og sidemenuen

I OS2-håndbogens Jekyll/Just the Docs-opsætning er **filens mappe** og **sidens placering i navigationen** ikke det samme. Navigationen styres blandt andet af YAML-blokken øverst i filen:

```yaml
---
title: Administrer tilmeldinger
layout: default
parent: Arrangementer
grand_parent: Værktøjskasse til projekter og produkter
nav_order: 50
has_children: false
has_toc: true
---
```

- `title`: Sidens menutitel.
- `parent` og eventuelt `grand_parent`: Sidens placering i sidemenuen.
- `nav_order`: Rækkefølgen på samme niveau. I OS2-håndbogen bruges normalt **10-spring**.
- `has_children`: Om siden er overordnet andre sider.

**Når du flytter en fil, opdateres YAML ikke automatisk – og omvendt.** Kontrollér derfor begge dele. Andre doc-sites kan have lidt andre indstillinger.

Retningslinjer for placering, indhold og godkendelse i OS2-håndbogen findes på siden **Skriv i håndbogen**.

### Se et hurtigt preview

1. Åbn en `.md`-fil.
2. Højreklik på filens **fane** øverst i editoren.
3. Vælg **Open Preview to the Side**.

Det viser formateret Markdown, men **ikke hele det færdige Jekyll-site** med sidemenu og design. Et fuldt lokalt Jekyll-preview kræver særskilt teknisk opsætning og er ikke nødvendigt for at følge denne guide.

## Gem og offentliggør ændringer

**Husk rækkefølgen:** Save → Stage → Commit → Push/Publish → Pull Request → Merge.

### 1. Gem og gennemse

1. Vælg **File → Save All**.
2. Klik på **Source Control** til venstre.
3. Kontrollér listen under **Changes**, især hvis du har slettet eller flyttet filer.

Bogstaverne ved filerne betyder typisk **M** = ændret, **U** = ny/ikke registreret i Git og **D** = slettet.

### 2. Stage og Commit i VS Code

1. Hold musen over overskriften **Changes**, og klik på **+** (*Stage All Changes*). Så flyttes ændringerne til **Staged Changes**.
2. Skriv en kort, sigende besked i feltet **Message**, fx `Opdater vejledning til nyhedsbreve`.
3. Klik på **Commit**.

Et **commit** registrerer ændringerne i din lokale versionshistorik. De er endnu ikke sendt til GitHub.

### 3. Send til GitHub (Push)

1. Klik på **Publish Branch**, **Publish Changes** eller **Sync Changes** i Source Control, afhængigt af hvad der vises.
2. Godkend eventuelle spørgsmål om login eller synkronisering.

Nu ligger dine ændringer på **din branch på GitHub**, men endnu ikke i `main`.

### 4. Opret Pull Request og Merge i browseren

1. Åbn det samme repository på **GitHub i browseren**.
2. Vælg **Compare & pull request**, hvis knappen vises. Ellers åbn **Pull requests → New pull request**.
3. Kontrollér, at ændringerne går **fra din branch til `main`**.
4. Beskriv kort, hvad du har ændret, og opret din pull request (PR).
5. Gennemse ændringerne, og få de godkendelser, der kræves. **Merge** først, når ændringerne er klar og må offentliggøres.

### 5. Opdater VS Code bagefter

1. Gå tilbage til VS Code.
2. Klik på branchnavnet nederst til venstre, og vælg **main**.
3. Klik på **Sync Changes**, eller vælg **… → Pull** i Source Control.

Nu er din lokale `main` opdateret, og du er klar til næste opgave.

## Hurtig huskeliste

- [ ] Skift til `main`, og opdater den, før du opretter en ny branch.
- [ ] Rediger på din branch, ikke på `main`.
- [ ] Gem med **File → Save All**.
- [ ] Kontrollér filerne under **Changes**.
- [ ] **Stage → Commit → Push/Publish** i VS Code.
- [ ] **Pull Request → Merge** i GitHub-browseren, efter relevant gennemgang.
- [ ] Skift til `main`, og **Sync/Pull** efter merge.

*Guiden beskriver en enkel, praktisk arbejdsgang. Hvis et repository har særlige regler, skal de følges.*