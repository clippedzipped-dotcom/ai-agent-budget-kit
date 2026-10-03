Bron: ONDERBROEKENZOEKER, StarNet-station, 2026-10-03. Alle claims met bron-URL.

# NL-compliance verdict — privépersoon verkoopt één digitaal playbook ($19) via eigen website

**Scope:** smalle vier-punts toets. Geen volledige compliance-verhandeling.
**Datum:** as-of dit onderzoek (bronnen: KVK 2026-09-15, Belastingdienst 2026-09-03/2026-09-23, ACM 2025-07-29 / ConsuWijzer 2026-07-22, wetten.overheid.nl BW 6 editie 2024-01-01).
**Methode:** live pagina-tekst opgehaald via Parallel Search connector (web_fetch en browser waren deze run onbruikbaar, zie "niet kunnen verifiëren").

---

## Wat er NU op de live pagina staat (geciteerd uit de opgehaalde paginatekst)

Source: https://ai-agent-budget-kit.netlify.app/

- Titel/claim: "AI Agent Budget Kit — Bouw een digitaal product met goedkope AI-modellen, verkoop het aan strangers op internet... Alles op deze pagina is gedaan met **€0 startbudget**".
- Product: "Eén markdown-document, 13.000+ tekens, direct te gebruiken" — 5 hoofdstukken + bijlage.
- Prijs: "**Koop de kit — $19**" (twee keer, boven en onder).
- **Beide koop-knoppen wijzen naar de letterlijke placeholder:** `https://ai-agent-budget-kit.netlify.app/__PAYPAL_PAYMENT_LINK__`
- Levering (footer): "Geleverd als markdown-bestand. Via Payhip krijg je na betaling direct een downloadlink; bij een losse PayPal-link stuur ik het bestand handmatig toe."
- FAQ weerlegt expliciet "Dit is een PDF?" → "Nee — markdown."
- FAQ "Wat als het niet werkt?" → "Het is een playbook, geen garantie."

**BELANGRIJK — afwijking van de LEAD CONTEXT:** de door mij opgehaalde paginatekst bevat **géén verkopersblok** ("Verkoper: Joey te Wierik, Nederland - clippedzipped@gmail.com"), **geen** checkbox voor uitdrukkelijke instemming, **geen** herroepingsrecht-tekst, **geen** btw-vermelding en **geen** cookie-verklaring. De lead-context claimde dat die live stonden. Ik kan alleen bevestigen wat de extractie teruggeeft: die elementen zitten niet in de opgehaalde tekst. Mogelijk staan ze in een niet-geëxtraheerd deel (bv. een formulier/JS-blok) — dat heb ik niet kunnen verifiëren. **Verder werk moet tegen de live pagina, niet tegen dit document of de lead-context.**

---

## 1. KVK — inschrijving verplicht?

**VERDICT: ACTIE NODIG** — toets de drie KVK-ondernemerscriteria serieus; bij structurele verkoop aan onbekenden via een eigen website is inschrijving waarschijnlijk verplicht, en niet-inschrijven is strafbaar.

KVK noemt drie cumulatieve criteria (alle drie = inschrijven): (1) je levert **zelfstandig** producten/diensten; (2) je vraagt een prijs **waarmee je geld verdient** (niet slechts kostendekking); (3) je levert **regelmatig aan anderen dan alleen familie/vrienden**.
Bron: https://www.kvk.nl/starten/moet-ik-mijn-bedrijf-inschrijven-bij-kvk/

De grens hobby/ondernemer volgens KVK's eigen voorbeelden: hobby = "af en toe", "klein bedrag voor de kosten", "alleen vrienden en familie" (voorbeeld Marek). Ondernemer = "steeds vaker bestellingen van onbekenden", "maakt reclame via social media", "maakt winst" (voorbeeld Kaitlen).
Bron: https://www.kvk.nl/starten/moet-ik-mijn-bedrijf-inschrijven-bij-kvk/

Gevolg bij niet-inschrijven terwijl je wél aan de criteria voldoet: overtreding van de Handelsregisterwet, **strafbaar op basis van de Wet Economische Delicten** — geldboete, taakstraf of gevangenisstraf.
Bron: https://www.kvk.nl/starten/moet-ik-mijn-bedrijf-inschrijven-bij-kvk/

**Twee losse rechtsgronden, niet door elkaar halen:** KVK hanteert de ondernemerscriteria voor het Handelsregister; de Belastingdienst heeft *eigen* ondernemerscriteria voor de inkomstenbelasting/btw. KVK geeft na inschrijving de gegevens door aan de Belastingdienst.
Bron: https://www.kvk.nl/starten/moet-ik-mijn-bedrijf-inschrijven-bij-kvk/

**Toepassing op deze case:** een eigen website met een verkoopknop, een prijs van $19 die geld oplevert, en levering aan willekeurige bezoekers ("strangers op internet" — de eigen woorden op de pagina) raakt criterium 2 en 3. Regelmaat (criterium 3) is het zwakste punt bij één enkel product, maar de opzet is publiek-onbeperkt en niet "alleen vrienden/familie". Dit is een grensgeval dat een professional moet toetsen; de veilige route is inschrijven.

---

## 2. BTW

**VERDICT: RISICO (hoog)** — de pagina vermeldt nergens btw en er is geen btw-positie gekozen; ook is "prijs inclusief btw" niet op de pagina te vinden (anders dan de lead-context stelde).

- **Registratiedrempel:** bij een jaaromzet van **maximaal € 2.200** én géén KVK-inschrijvingsplicht kun je de registratiedrempel gebruiken. **Maar:** ben je verplicht in te schrijven bij KVK, of heb je je al eerder als btw-ondernemer aangemeld, dan geldt de drempel **niet**, ook niet onder € 2.200.
  Bron: https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/zakelijk/btw/hoe_werkt_de_btw/kleineondernemersregeling/registratiedrempel-voor-kleine-ondernemers
- **KOR (kleineondernemersregeling):** omzet **niet meer dan € 20.000 per kalenderjaar** → btw-vrijstelling. Deelnemer **mag geen btw berekenen**, doet **geen btw-aangifte** en kan **geen btw terugvragen**.
  Bron: https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/zakelijk/btw/hoe_werkt_de_btw/kleineondernemersregeling/kleineondernemersregeling
- **EU-KOR sinds 1 januari 2025:** deelnemers kunnen een btw-vrijstelling krijgen voor 1 of meer EU-landen waar zij zakendoen. Relevant omdat de prijs in **USD** staat en de koper mogelijk buiten NL zit.
  Bron: https://www.belastingdienst.nl/wps/wcm/connect/bldcontentnl/belastingdienst/zakelijk/btw/hoe_werkt_de_btw/kleineondernemersregeling/kleineondernemersregeling
- **Mag/moet je "btw" vermelden zonder btw-plicht?** Een KOR-deelnemer **mag geen btw berekenen** en dus ook niet als "btw" op de pagina/factuur zetten. Consumentenprijzen moeten inclusief alle belastingen zijn als er wél btw verschuldigd is.
  Bron (KOR-verbod): zie Belastingdienst KOR hierboven. (De expliciete regel "prijzen inclusief btw vermelden bij btw-plicht" heb ik op belastingdienst.nl in deze run niet op een eigen pagina kunnen lezen — zie "niet kunnen verifiëren".)

**Praktische kern:** of je nu onder de registratiedrempel valt, onder de KOR, of volledig btw-plichtig bent — in **alle drie** de gevallen mag er **geen** btw-opbouw op de pagina staan zoals nu geïmpliceerd ("$19"), tenzij je btw-plichtig bent en het bedrag inclusief btw is. Kies eerst je positie, vermeld die positie dan pas.

---

## 3. Herroepingsrecht bij digitale content

**VERDICT: ACTIE NODIG** — de wettelijke uitsluiting bestaat, maar vereist **drie** cumulatieve voorwaarden die op de live pagina niet zijn aangetroffen.

Wetsartikel: **art. 6:230p BW** (Boek 6, titeldeel 5, afdeling 2b, paragraaf 3).
Bron: https://wetten.overheid.nl/BWBR0005289/2024-01-01

De relevante uitzondering is **lid 1, onderdeel g**: geen recht van ontbinding bij "een overeenkomst voor de levering van digitale inhoud die niet op een materiële drager is geleverd" — **voor zover aan álle drie**:
1. de nakoming is begonnen met **uitdrukkelijke voorafgaande toestemming** van de consument;
2. de consument heeft **verklaard dat hij daarmee afstand doet van zijn recht van ontbinding**;
3. de handelaar heeft een **bevestiging verstrekt** als bedoeld in art. 6:230t lid 2 of art. 6:230v lid 7.

Daarnaast verplicht **art. 6:230m** tot informatie die óók de afstandsituatie dekt, waaronder (lid 1, onderdeel h) een **modelformulier voor ontbinding** en de bedenktijdinformatie.
Bron: https://wetten.overheid.nl/BWBR0005289/2024-01-01

Bevestiging door de ACM (ConsuWijzer): bij online aankopen recht op "informatie over uw bedenktijd", "een zogenoemd 'modelformulier voor ontbinding'", en een kopie van het contract. En: "Soms is het bedrijf verplicht om u te laten weten dat u géén bedenktijd hebt."
Bron: https://consument.acm.nl/aankoop-dienst-annuleren/verplichte-informatie-bij-koop-product-dienst

**Wat concreet op de pagina/checkout moet staan:** (a) dat er normaal 14 dagen bedenktijd geldt; (b) dat bij digitale content het herroepingsrecht **vervalt** zodra de download start; (c) dat dit alleen gebeurt na **uitdrukkelijke voorafgaande toestemming** én de **verklaring van afstand** van de klant; (d) een **bevestiging** daarvan aan de klant (art. 6:230t lid 2). Een simpele checkbox vóór betaling die beide elementen dekt, plus een bevestigingsmail, is de kortste route.

---

## 4. Verplichte verkopersinformatie

**VERDICT: ACTIE NODIG** — naam + land + e-mail is **niet** genoeg volgens de ACM; er is minimaal een **bezoekadres** en **telefoonnummer** of klachtenadres nodig.

ACM, "Consumenten informeren": "Verplichte bedrijfsgegevens moeten makkelijk te vinden zijn, zoals naam, e-mailadres en telefoonnummer."
Bron: https://www.acm.nl/nl/verkoop-aan-consumenten/consumenten-informeren

ACM ConsuWijzer, uitputtende lijst "Informatie over het bedrijf": de **naam van het bedrijf**; het **bezoekadres**; het **adres voor klachten**; het **telefoonnummer en e-mailadres**; uitleg over hoe hij met persoonsgegevens omgaat. Bovendien: "of degene van wie u koopt een **bedrijf of een consument** is" en "dat u **geen consumentenrechten heeft als u van een consument koopt**".
Bron: https://consument.acm.nl/aankoop-dienst-annuleren/verplichte-informatie-bij-koop-product-dienst

ACM over het aanbod: in het aanbod moet in elk geval **bedrijfsnaam en vestigingsadres**, belangrijkste kenmerken, prijs en bijkomende kosten, recht op bedenktijd, en recht op annuleren staan. Informatie moet **makkelijk vindbaar** zijn, "dus niet verstopt in bijvoorbeeld algemene voorwaarden".
Bron: https://www.acm.nl/nl/verkoop-aan-consumenten/consumenten-informeren/verplichte-informatie-voor-en-na-de-koop

Wettelijke basis voor de bedrijfsgegevens: **art. 6:230m BW** (informatieplicht vóór het sluiten van de overeenkomst), en voor de herkomst **art. 6:230b** (o.a. naam, vestigingsadres en, bij een gereglementeerd beroep, registerinschrijving en nummer).
Bron: https://wetten.overheid.nl/BWBR0005289/2024-01-01

**Belangrijke nuance — dit is de kern van de zaak:** de verhoogde consumentenbescherming (bedenktijd, modelformulier) hoort bij de **handelaar** ("handelaar: natuurlijk persoon of rechtspersoon die handelt in de uitoefening van een beroep of bedrijf", art. 6:193a lid 1 onder b BW). Verkoop je als **consument aan consument**, dan moet je dat wél melden ("u heeft geen consumentenrechten als u van een consument koopt") — maar de bedenktijd-verplichting valt weg, en juist dán wordt de KVK-vraag uit punt 1 beslissend. Je kunt niet én "privépersoon" claimen om de herroepingsregels te ontwijken én tegelijk een publieke webshop met bedrijfsuitstraling runnen. Kies één positie consistent.
Bron: https://wetten.overheid.nl/BWBR0005289/2024-01-01 (art. 6:193a lid 1 onder b)

---

## 5 actiepunten (in volgorde)

1. **Repareer de koopknop.** Beide knoppen wijzen naar `__PAYPAL_PAYMENT_LINK__` — een niet-vervangen template-placeholder. Er kan nu niets verkocht worden. Dit is functioneel blokkerend, vóór elke compliance-vraag. (Geen PayPal-tool gebruiken; losse link of Payhip, zie footer-tekst.)
2. **Kies één juridische positie en maak hem consistent.** Ofwel privépersoon/C2C (dan: expliciet melden dat er geen consumentenrechten zijn, geen bedrijfsuitstraling, KVK-toets), ofwel ondernemer (dan: KVK-inschrijving, btw-positie, volledige bedrijfsgegevens). De huidige pagina mengt beide.
3. **Zet de vier ontbrekende info-elementen op de pagina:** bezoekadres, klachtenadres, telefoonnummer, en de privacy-uitleg over persoonsgegevens — plus kenmerken/prijs/levering die er al deels staan. Naam + land + e-mail is aantoonbaar te weinig.
4. **Bouw de afstandsverklaring correct in de checkout:** 14-dagen bedenktijd vermelden, aparte checkbox met (a) uitdrukkelijke voorafgaande toestemming tot directe levering én (b) verklaring van afstand van het recht van ontbinding, en stuur daarna een bevestiging (art. 6:230t lid 2 BW). Zonder alle drie de elementen blijft het herroepingsrecht gewoon bestaan.
5. **Leg de btw-positie vast en vermeld die positie.** Bepaal of je onder de registratiedrempel (≤ € 2.200 én niet KVK-inschrijvingsplichtig), onder de KOR (≤ € 20.000) valt of volledig btw-plichtig bent. Zet daarna geen btw-opbouw op de pagina tenzij je btw-plichtig bent en de prijs inclusief btw is. Let op EU-KOR sinds 1-1-2025 bij verkoop in USD aan kopers buiten NL.

---

## Niet kunnen verifiëren

- **De live pagina was niet met eigen ogen te lezen.** `web_fetch` faalde 4× op alle URL's ("fetch failed"); `browser_navigate` werd geweigerd ("station browser profile is in use by another agent run"). De paginatekst hierboven komt uit de Parallel Search-connector-extractie, niet uit een door mij gerenderde pagina. JS- of formulier-inhoud kan daardoor ontbreken.
- **Daarom: het verkopersblok, de instemmings-checkbox, de herroepingsrecht-tekst, de btw-vermelding en de cookie-verklaring die de lead-context als "live" opvoerde, heb ik in mijn extractie NIET teruggevonden.** Ik kan niet bevestigen dat ze live staan; ik kan alleen bevestigen dat ze niet in de opgehaalde tekst zitten. Verifieer dit visueel in de browser voordat er conclusies aan hangen.
- **ACM-pagina "bedrijfsgegevens vermelden"** (`/consumenten-informeren/bedrijfsgegevens-vermelden`) is niet apart opgehaald; de lijst hierboven komt van de ConsuWijzer-pagina. Twee ACM-bronnen bevestigen dezelfde strekking, maar het exacte formulier van de bedrijfsgegevens-verplichting is niet uit de primaire ACM-subpagina gelezen.
- **De expliciete regel "prijzen inclusief btw vermelden"** (art. 6:230m lid 1 / Richtlijn 98/6/EG prijsaanduiding) heb ik in deze run niet op een eigen Belastingdienst-pagina teruggelezen. De KOR-regel ("mag geen btw berekenen") is wél uit primaire bron bevestigd.
- **Geen juridisch advies.** Dit is bronwerk, geen advocatenmening. De KVK-grens en de C2C/handelaar-kwalificatie zijn grensgevallen die een jurist moet toetsen.
- **Drempelbedragen zijn as-of de bronpublicatiedata hierboven** (Belastingdienst-pagina's gedateerd 2026-09-03 resp. 2026-09-23, KVK 2026-09-15). Bedragen kunnen per kalenderjaar wijzigen — hertoets bij een nieuw jaar.
