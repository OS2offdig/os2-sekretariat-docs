---
title: Processer og rutiner
layout: default
nav_order: 5
has_children: true
has_toc: false
---

# Processer og rutiner  
Her samles og beskrives de faste arbejdsgange, som sikrer kvalitet, ensartethed og overblik i sekretariatets drift og projekter. Afsnittet supplerer OS2’s governance-model og fungerer som både arbejdsgrundlag for sekretariatets daglige praksis og orientering for produktkoordinatorer, bestyrelse og samarbejdspartnere.


## Onboarding af nye medarbejdere {#onboarding}
Nye medarbejdere introduceres gennem et forløb, der kombinerer ITK’s fælles onboarding med OS2’s egne introduktioner til værktøjer, produkter og governance. Detaljeret proces og tjekliste findes i særskilt dokument:  

- [Onboarding af nye medarbejdere (ToDO)](processes/onboarding_medarbejder)


## Budgetstyring og økonomiprocesser {#budgetstyring}
Sekretariatet håndterer foreningens, OS2-projekter og -produkters økonomi i samarbejde med **ITK’s stab og økonomifunktion i Aarhus Kommune**, som varetager bogføring, betaling og regnskabsaflæggelse. OS2’s tilslutningsaftaler og **takstmodel** fastlægger bidrag og fordeling af de økonomiske bidrag til forening og produkter: [takstblade.os2.eu](https://takstblade.os2.eu).

**Sekretariatets rolle**
- Fremlægge årsregnskab for bestyrelsen samt generalforsamling.  
- Fremlægge regnskabsstatus og årsregnskab for projekter og produkter.    
- Udarbejde forslag til årsbudget og fremlægge det for bestyrelsen samt generalforsamling.  
- Koordinere budget, regnskab og økonomiske dispositioner med bestyrelse, produktkoordinatorer og styregrupper.  
- Håndtere tilslutninger til produkter og tilsagn til projekter, herunder økonomien.  
- Sikre sammenhæng mellem budget, medlemsbidrag og produktmidler.  
- Opdatere økonomioverblik på tværs af projekter og produkter kvartalsvis eller ved væsentlige ændringer.  

**Principper**
- Alle økonomiske beslutninger skal kunne spores til godkendelse i styregruppe, bestyrelse eller generalforsamling. Ofte sker den formelle godkendelse via det godkendte budget og et delegeret mandat til sekretariatschef eller produktkoordinator.  
- Økonomidata gemmes i Nextcloud under mappen *Økonomi*.  
- Stamdata som ligger til grund for økonomien trækkes fra Airtable.  
- Budgetopfølgning indgår fast som punkt på styregruppemøder og bestyrelsesmøder.  


## Fakturahåndtering og godkendelsesflow {#faktura}
Fakturabehandling følger den procedure, der er beskrevet i *[Oversigt over fakturagodkendere](processes/os2_faktura_godkender)*.  
Grundprincippet er to-trins-godkendelse: én person kontrollerer, en anden godkender.

**Procesoversigt**
1. Faktura til OS2 modtages via ITK’s system (OS2 EAN: 5790002750595).  
2. Sekretariatet kontrollerer fakturaens indhold, beløb, bilag og kontering.  
3. Fakturaen sendes til korrekt godkender jf. [oversigten](processes/os2_faktura_godkender).  
4. Godkendelsen registreres og dokumenteres jf. [kontoplan](processes/os2_kontoplaner).  
5. Betaling håndteres af ITK’s økonomifunktion.  

**Dokumentation**
- Fakturaer arkiveres i ITK's økonomisystem.  
- Ved produkt- og projektspecifikke udgifter henvises til issue ID i projektets eller produktets backlog (issue-tracker på Github eller Jira).  
- Godkendelseslisten opdateres årligt eller ved ændringer i bemanding.


## Time- og opgaveregistrering {#time}
Sekretariatet anvender **Leantime** til registrering af tid og opgaver.  
Formålet er at skabe overblik over ressourceforbrug, sikre transparens og understøtte rapportering.

**Grundprincipper** (fra struktur for tidsregistrering):
- **Projekt = hvor** du arbejder (OS2-projekt, OS2-produkt eller sekretariatsprojekt, -ydelsesområde).  
- **Opgave (to-do) = hvad** du laver (kort titel på opgaven, [se eksempler](processes/task_examples)).  
- **Tag = type** kategori for det du laver (rådgivning, koordinering, drift, kommunikation osv.).
- **Tid = hvor længe** du har brugt (i kvarte timer).  

**Regler**
- Én registrering = ét projekt + én opgave (to-do) med tilknyttet tag.  
- Registrer på sekretariatsprojekt, - ydelsesområde hvis en opgave vedrører flere OS2-projekter eller -produkter.  
- Brug faste projektnavne og tags (opgavetyper) som defineret i strukturen.  
- Intern tid (ferie, fravær, pauser, møder uden projekter osv.) registreres under *OS2 intern tid*.  

Detaljeret vejledning findes i:  
- [Struktur for tidsregistrering](processes/os2_tidsregistrering).


## Udbud, kontrakter og juridiske processer {#udbud}
Sekretariatet understøtter produkter og projekter i **kontraktmæssige spørgsmål**, men OS2 udarbejder ikke selv udbudsmateriale og kan ikke rådgive om jura.  

I stedet anvendes:
- **OS2’s governance-model** som ramme for lovlighed, åbenhed og dokumentation.  
- **[SKI (Statens og Kommunernes Indkøbsservice)](https://ski.dk)** som indkøbsfællesskab, hvor OS2 er medlem.  
- **Andre fællesskaber** som f.eks. Det fælles [databehandlersekretariat](https://kommunedbs.dk/).
- **Eksterne kompetencer** jurister og andre rådgivere efter behov.  

**Proces og rollefordeling**
1. Behov drøftes med sekretariatet.  
2. Sekretariatet vurderer omfang, relation til governance og eventuel SKI-aftale.  
3. Ved behov for udbud/kontraktstøtte involveres relevante aktører (fx ekstern rådgiver eller kommunal jurist).  
4. Sekretariatet sikrer, at dokumentation, licensvalg og kontraktmateriale arkiveres i produktets Nextcloud mappe og/eller Git-repo.  

**Principper**

- **Open source som standard:**  
  OS2’s standard for open source-licenser (MPL 2.0) skal som udgangspunkt anvendes, medmindre der er tungtvejende grunde til at vælge en anden OSI-godkendt licens. Licensvalget skal altid fremgå af produktets governance-rapport.  

- **OS2 FLOSS-aftalen:**  
  Alle udviklings- og samarbejdsaftaler skal medtage OS2’s **[FLOSS-aftale](https://boks.os2.eu/s/L7PArJkrBcpnWe8)**, som fastlægger de juridiske rammer for samarbejde, licensering, rettighedsforhold og offentliggørelse af kildekode.  
  FLOSS-aftalen bruges til at sikre, at alle parter – offentlige og private – arbejder under fælles open source-principper og med tydelig afklaring af ansvar, roller og ejerskab.

- **Ophavsret og overdragelse:**  
  Ved aftaler med leverandører eller eksterne udviklere skal der indgås en **ophavsrets- eller rettighedsoverdragelsesaftale**, der sikrer, at kildekoden og eventuelle relaterede materialer overdrages til OS2-fællesskabet.  
  OS2 skal have de fulde rettigheder til at videreudvikle, udvide og distribuere løsningen under open source-licensen, uanset hvilken leverandør der har leveret arbejdet.

- **Ejerskab og opfølgning:**  
  Alle kontrakter og aftaler skal have et tydeligt ejerskab og defineret opfølgningsansvar, typisk hos produktets styregruppe eller sekretariatet.  
  Der skal fremgå, hvem der har ansvaret for at overvåge licens- og kontraktmæssig overholdelse.

- **Dokumentation:**  
  Juridiske vurderinger, licensvalg og kontrakter dokumenteres i produktets **governance-rapport** og arkiveres i GitHub og/eller Nextcloud, så der altid er åbenhed og sporbarhed.

- **Afgrænsning**
  Sekretariatet yder ikke juridisk assistance, men rådgiver om, at OS2’s fælles principper for open source, rettigheder og governance følges i alle samarbejder.


## Sammenfatning
Sekretariatets processer og rutiner skal sikre **ensartet kvalitet, gennemsigtighed og effektiv drift** – og skabe tillid på tværs af fællesskabet.  
De understøtter OS2’s værdisæt: *åbenhed, samarbejde og fælles ejerskab*.  
Når vi arbejder systematisk og dokumenteret, kan vi samtidig være fleksible, lydhøre og eksperimenterende – i OS2’s ånd.
