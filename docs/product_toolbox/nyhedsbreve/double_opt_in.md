---
title: Opsæt double opt-in
layout: default
parent: Nyhedsbreve
nav_order: 20
has_toc: false
---

# Opsæt double opt-in i Heyloyalty

OS2 bruger som udgangspunkt double opt-in (DOI) ved frivillig tilmelding til produktnyhedsbreve.

Double opt-in betyder, at personen først tilmelder sig og derefter bekræfter tilmeldingen via en mail.

> **Bemærk**
>
> Denne guide beskriver OS2's anbefalede arbejdsgang i Heyloyalty.
>
> Heyloyalty kan løbende ændre funktioner, menuer og muligheder. Tjek derfor altid [Heyloyaltys officielle guides](https://guides.heyloyalty.com/) ved tvivl eller hvis noget i denne vejledning ikke stemmer med det, du ser i systemet.
>
> Hvis Heyloyaltys dokumentation og denne guide er forskellige, er Heyloyaltys aktuelle dokumentation gældende for den tekniske funktionalitet.

> **💡 Sådan finder du listeindstillingerne**
>
> Det er ikke nok at klikke ind på selve listen.
>
> Gå til **Lister** og klik på **de tre små prikker helt ude til højre ud for den relevante liste**. Herfra kan du vælge at redigere listen og finde indstillinger for bl.a. double opt-in og formularer.

## 1. Aktivér double opt-in på listen

Gå til:

**Lister → ⋮ ved den relevante liste → Rediger liste → Dobbelt opt-in**

Aktivér double opt-in på listen.

## 2. Opret DOI-automationen

Gå til **Automations** og opret et nyt automationflow.

Vælg:

- den relevante produktliste
- trigger: **Dobbelt opt-in**

Opret derefter den mail, der skal sendes, når en person tilmelder sig.

### Minimum for bekræftelsesmailen

**Emnelinje:**

`Bekræft din tilmelding til [produktnavn]`

**Preheader:**

`Klik for at bekræfte, at du vil modtage nyt om [produktnavn]`

**Mailtekst:**

> **Bekræft din tilmelding**
>
> Tak for din interesse i [produktnavn].
>
> Klik på knappen nedenfor for at bekræfte, at du vil modtage nyheder og information om produktet.
>
> **Bekræft tilmelding**
>
> Hvis du ikke selv har tilmeldt dig, kan du bare se bort fra denne mail.

Bekræftelsesknappen skal bruge Heyloyaltys double opt-in-flettefelt:

`{member.doubleOptin}`

## 3. Opsæt siderne i DOI-flowet

Under listens double opt-in-indstillinger findes siderne, som vises efter bekræftelseslinket.

Du kan tage udgangspunkt i følgende tekster:

### Tak for bekræftelse

> **Så er du med!**
>
> Din tilmelding til nyhedsbrevet om [produktnavn] er nu bekræftet. Du vil fremover modtage nyt om produktet, udviklingen og fællesskabet.

### Der opstod en fejl

> **Noget gik galt**
>
> Vi kunne ikke bekræfte din tilmelding. Prøv igen, eller kontakt OS2, hvis problemet fortsætter.

### Tilmeldingsfrist udløbet

> **Linket er udløbet**
>
> Bekræftelseslinket er ikke længere gyldigt. Tilmeld dig nyhedsbrevet igen for at få et nyt link.

## 4. Test hele flowet

En almindelig testmail er **ikke tilstrækkelig til at teste double opt-in-linket**.

Flettefeltet `{member.doubleOptin}` bliver først til et personligt bekræftelseslink i forbindelse med en reel tilmelding.

Test derfor med en e-mailadresse, der ikke allerede står på listen:

1. Tilmeld dig via produktets tilmeldingsformular.
2. Kontrollér, at DOI-mailen kommer frem.
3. Klik på bekræftelseslinket.
4. Kontrollér, at bekræftelsessiden vises korrekt.
5. Kontrollér i Heyloyalty, at kontakten er blevet tilmeldt.

## Manuel import

Ved manuel oprettelse / import af kontakter, kan du markere "Opret kontakt uden dobbelt opt-in bekræftelsesmail" og "Opret kontakt uden velkomst-trigger-mail" når du gennemgår import-flowet. 
	
---

**👀 Kan du ikke finde listeindstillingerne?**  
Du skal **ikke klikke ind på selve listen**.

**Lister → ⋮ helt ude til højre ved listen → Rediger liste**

Her finder du bl.a. felter, formularer og double opt-in.
{: .highlight }
