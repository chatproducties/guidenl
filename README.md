# Chatwize — Documentatie / Docs

Klantgerichte handleiding voor Chatwize, gebouwd met [Mintlify](https://mintlify.com).
Tweetalig: Engels (`en/`) en Nederlands (`nl/`).

Deze docs leggen uit **hoe je Chatwize gebruikt**: waar je klikt, wat je instelt
en hoe je je chatbot live krijgt.

## Structuur

```
docs.json          Mintlify-configuratie (navigatie, talen, huisstijl)
en/                Engelse pagina's (.mdx)
nl/                Nederlandse pagina's (.mdx)
images/            Schermafbeeldingen, per taal (en-*.png / nl-*.png)
logo/              Logo (light/dark)
favicon.svg        Favicon
```

De navigatie en talenswitcher staan volledig in `docs.json` onder
`navigation.languages`.

## Lokaal bekijken

Je hebt Node.js nodig. Installeer de Mintlify CLI en start de preview:

```bash
npm i -g mint      # eenmalig
cd chatwize-docs
mint dev           # opent http://localhost:3000
```

Bewerk een `.mdx`-bestand en de browser herlaadt automatisch.

Controleer op kapotte links:

```bash
mint broken-links
```

## Schrijfrichtlijnen

- **Handleiding, geen marketing.** Beschrijf waar iemand klikt en wat er
  gebeurt. Geen verkooppraat, geen "voor wie is het".
- **Geen prijzen of abonnementslimieten.** Die staan op chatwize.ai en
  veranderen te vaak om hier te dupliceren. Is een functie afhankelijk van het
  abonnement, verwijs dan naar de prijzenpagina in plaats van een plannaam te
  noemen.
- **Geen techniek onder de motorkap.** Geen leveranciers, modelnamen,
  architectuur of interne werking.
- **Beveiligings- en privacyvragen** worden per klant beantwoord via
  hello@chatwize.ai.
- **Noem geen getallen** voor limieten en drempels die per abonnement of per
  instelling verschillen; beschrijf het gedrag.

## Aanpassen

- **Kleuren / merk** — `colors` in `docs.json`.
- **Logo / favicon** — vervang de bestanden in `logo/` en `favicon.svg`.
- **Beelden** — schermafbeeldingen van het live dashboard, apart per taal
  (`nl-*.png` en `en-*.png`). Na een UI-wijziging: maak een nieuwe
  schermafbeelding en overschrijf het bestand met dezelfde naam, in **beide**
  talen. Gebruik altijd een leeg testaccount, nooit een klantomgeving, en
  controleer vóór het opslaan dat er geen widget-sleutel, deelbare link,
  e-mailadres of klantnaam in beeld staat.
- **Navigatie** — de `groups`/`pages`-lijsten per taal in `docs.json`.
- **Links naar het product** — het dashboard is `https://eu.chatwize.ai`, de
  marketingsite `https://chatwize.ai`, support is `hello@chatwize.ai`.

## Een pagina toevoegen

1. Maak `en/mijn-pagina.mdx` én `nl/mijn-pagina.mdx` met frontmatter (`title`,
   `description`).
2. Voeg het pad (zonder `.mdx`) toe aan de juiste taalgroep in `docs.json`.

Houd de EN- en NL-versies inhoudelijk gelijk zodat beide talen compleet blijven.
Controleer na een release of de UI-labels in de docs nog kloppen met de app —
de teksten verwijzen naar concrete knoppen en sectienamen.
