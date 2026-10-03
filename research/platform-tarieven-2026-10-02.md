# Platform-tarieven — aanvulling op research/betaalplatform-feiten.md

Datum: 2026-10-02
Scope: **alleen wat nog niet in `research/betaalplatform-feiten.md` staat.**
Die cijfers voor Payhip, Gumroad, Lemon Squeezy, Ko-fi, Mollie en Stripe zijn daar al vastgelegd — dat bestand wordt hier niet herhaald.

Dit bestand voegt twee dingen toe:
1. **Etsy** (stond in geen enkel bestand; de cijfers kwamen uit mijn vorige antwoord).
2. **De verwerkerlaag** — expliciet welke platforms een aparte payment-processor bovenop of ín de platformfee rekenen.

Methode: live gelezen op 2026-10-02 via de MCP web-extractie (`web_fetch` gaf "fetch failed"; de station-browser was bezet).

---

## 1. Etsy — de cijfers en waar ze LETTERLIJK staan

### 1a. Transactiefee 6,5% en listingfee $0,20 (USD)

- **Bron-URL:** https://www.etsy.com/legal/fees/
- **Sectienummer:** **"1. Types of Fees"** → subsectie **"Transaction Fees"**, en de listingfee één subsectie eerder: **"Listing Fees"**.
- **Letterlijk (Transaction Fees):** *"When you make a sale through Etsy.com, you will be charged a transaction fee of 6.5% of the price you display for each listing plus the amount you charge for shipping and gift wrapping."*
- **Letterlijk (Listing Fees):** *"You will be charged a listing fee of $0.20 USD for each item that you list for sale on Etsy.com or Etsy's mobile apps."*
- **Belangrijk detail uit dezelfde sectie:** de transactiefee geldt óók op verzendkosten en op de belasting die in je prijs zit. Letterlijk: *"If you sell from anywhere other than the US, the transaction fee will apply to the listing price (which should include any applicable taxes that you as a seller are responsible for), shipping price, and gift wrapping fee."* — Voor Nederland betekent dat: btw die jij in de prijs verwerkt, wordt ook befeet.
- **Laatst bijgewerkt:** pagina vermeldt *"Last updated on Oct 5, 2026"*.
- **Listingduur/auto-renew:** *"Etsy.com listings expire after four months."* Auto-renew kost opnieuw $0,20 per listing.

### 1b. Payment processing 4% + €0,30 (Nederland)

- **Bron-URL:** https://www.etsy.com/legal/etsy-payments/
- **Sectienummer:** **"9. Payment Processing Fees"** → subsectie **"B. Fee Amount"** (de landentabel).
- **Letterlijke rij:** `| Netherlands | 4% + 0.30 EUR | |`
- **Letterlijke kolomkop:** *"Etsy Payments Fees (% of total sale price + flat fee per order) exclusive of VAT, where applicable"*
- **Grondslag waarover de fee gaat (sectie 9A):** *"The fee amount will be assessed on the gross order amount, including shipping and tax (if applicable)."*
- **NL is ondersteund:** Nederland staat in de lijst Etsy Payments-landen in sectie 2: *"...Malta, Mexico, Morocco, Netherlands, New Zealand..."*
- **Laatst bijgewerkt:** pagina vermeldt *"Last updated on Jul 31, 2026"*.

> **Antwoord op de directe vraag van de lead:** 6,5% → `https://www.etsy.com/legal/fees/`, sectie **1 → "Transaction Fees"**. $0,20 → zelfde pagina, sectie **1 → "Listing Fees"**. 4% + €0,30 → `https://www.etsy.com/legal/etsy-payments/`, sectie **9 → "B. Fee Amount"** (rij Netherlands). Fees zijn **exclusief btw**.

### 1c. Doorrekening op één verkoop van ~$19 (≈ €17,50)

Reken zelf de koers niet om in het rapport — de platformfees rekenen in hun eigen valuta, dus hier beide.

| Fee | Bedrag op een €17,50-verkoop |
|---|---|
| Listingfee | $0,20 |
| Transactiefee 6,5% (over prijs + verzending + inbegrepen belasting) | ≈ $1,24 |
| Payment processing (NL) 4% + €0,30 | ≈ €1,00 |
| **Totaal** | **≈ $1,44 + €1,00 ≈ €2,30** |

Netto ≈ **€15,20 van €17,50**. Dat is ~13% van de omzet — en dat is nog **exclusief** eventuele btw-afdracht, de 2,5% currency conversion fee (sectie 9C, als je in een andere valuta list dan je uitbetaalrekening) en optionele Offsite Ads (12% of 15%, sectie 1 → "Advertising and Promotional Fees").

**Niet gevonden op https://www.etsy.com/legal/fees/:** geen uitspraak over of je een KVK- of btw-nummer nodig hebt om er te verkopen. De pagina zegt alleen wie de btw op verkopersfees afdraagt en dat Etsy in bepaalde landen btw op digitale leveringen int en afdraagt (sectie 5C → "Digital VAT Fees"): *"Under local laws in certain countries, Etsy is required to collect and remit VAT to the relevant tax authorities when you sell a digital item delivered via automatic download to the buyer."* Dat gaat over de btw **namens de koper**, niet over vrijstelling van KVK-inschrijving.

---

## 2. De verwerkerlaag — wie rekent wat bovenop of ín de fee

Dit is het punt dat in `betaalplatform-feiten.md` wel per platform genoemd staat, maar niet als aparte laag naast elkaar. Voor een $19-verkoop is dat het verschil tussen "5% fee" en "5% + 2,9% + vast bedrag".

### A. Één laag — de processor zit ín de platformfee

| Platform | Wat de pagina zegt | Bron |
|---|---|---|
| **Etsy** | Etsy Payments ís de processor. Geen aparte Stripe/PayPal-laag: *"there is no additional PayPal fee"* voor integrated PayPal. Voor standalone PayPal geldt: *"Sellers who accept standalone PayPal will continue to pay PayPal fees."* | https://www.etsy.com/legal/etsy-payments/ sectie 3 |
| **Gumroad** | Geen aparte processorlaag genoemd bovenop de 10% + $0,50. | https://gumroad.com/pricing |
| **Lemon Squeezy** | Geen aparte processorlaag; wel "edge cases waar kleine extra fees gelden" en +0,5%–1% voor extra betaalmethoden. | https://www.lemonsqueezy.com/pricing |
| **Mollie** | Mollie is zelf de payment provider — de tarieven (iDEAL €0,32, kaart 1,80% + €0,25) zijn de enige laag. | https://www.mollie.com/pricing |
| **Stripe** | Stripe is zelf de provider; Payment Links heeft geen extra abonnement. | https://stripe.com/nl/payment-links |

### B. Twee lagen — je betaalt de platformfee ÉN de processor

| Platform | De laag erbovenop (letterlijk) | Bron |
|---|---|---|
| **Payhip** | *"Yes, PayPal and Stripe will still charge at their standard rates once they complete a transaction. This applies for all plans."* → 5% Payhip + Stripe/PayPal. | https://payhip.com/pricing |
| **Ko-fi** | *"You only pay the service fees (no more than 5%) plus standard payment processor fees."* én *"you'll need to connect your Ko-fi to a PayPal or Stripe account to get paid."* → 5% Ko-fi + Stripe/PayPal. | https://ko-fi.com/pricing |

### C. De verwerkerlaag zelf — percentages

Voor Payhip en Ko-fi komt de tweede laag dus van **Stripe of PayPal**. Die tarieven staan niet in `betaalplatform-feiten.md`, want dat bestand las alleen de zes platformpagina's.

**Niet gevonden op https://payhip.com/pricing en https://ko-fi.com/pricing:** het percentage dat Stripe of PayPal rekent. Beide pagina's verwijzen naar "standard rates" zonder ze te noemen. Ik heb die tarieven in deze run niet opgezocht — dat viel buiten de opdracht ("alleen nog afmaken").

---

## 3. Merchant of record — aanvulling

`betaalplatform-feiten.md` noemt Gumroad, Lemon Squeezy en Payhip als merchant of record, en Mollie, Stripe en Ko-fi als niet-MoR. Voor Etsy geldt op basis van de gelezen pagina's:

- Etsy is **geen klassieke merchant of record** voor de btw op jouw omzet: *"Aside from the limited circumstances set out below, you are responsible for collecting and paying any taxes associated with using and making sales through Etsy's services"* (sectie 5).
- Etsy treedt wel op als **incassomakelaar**: *"Each seller appoints Etsy as its agent for the purpose of receiving, holding, and settling payments to seller"* (sectie 6).
- En Etsy draagt btw op **digitale downloads** af in landen waar dat wettelijk moet (sectie 5C, hierboven geciteerd).

Praktisch gevolg voor de kit: op Etsy blijft de btw-vraag in principe bij jou liggen, met uitzondering van de digital-VAT-regeling die Etsy beschrijft.

---

## 4. Bronnen (live gelezen, 2026-10-02)

- https://www.etsy.com/legal/fees/ — secties 1 ("Listing Fees", "Transaction Fees", "Advertising and Promotional Fees"), 5 (Taxes)
- https://www.etsy.com/legal/etsy-payments/ — secties 2 (Overview/dekking), 3 (Third-Party Services), 6 (Collection Agent), 9 ("Payment Processing Fees", "B. Fee Amount")
- Voor Payhip, Gumroad, Lemon Squeezy, Ko-fi, Mollie en Stripe: zie `research/betaalplatform-feiten.md` (daar staan de citaten en URL's al).

**Wat ik NIET heb geverifieerd:** de Stripe- en PayPal-verwerkertarieven die Payhip en Ko-fi doorberekenen; of Etsy een KVK-nummer eist bij aanmelding; of Etsy shops toestaat die uitsluitend een digitaal bestand verkopen.
