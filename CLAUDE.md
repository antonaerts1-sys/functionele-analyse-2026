# Functionele analyse 2026 — de to-be

Deze folder bevat drie visualisaties en deze methodologie-doc over hoe functionele analyse er anno 2026 idealiter uitziet voor development projecten.

## Wat hier ligt

- `index.html` — de zes-fase flow met AI-rollen per fase (discovery → validatie)
- `touchpoints.html` — swim-lane met klant, analist, dev. Handovers en rituelen.
- `to-be.html` — de centrale to-be in één beeld: trio, loop, outcome, AI-laag
- `maandfocus.html` — het werkdocument: per fase skills, acties deze maand en historiek, plus één teamfocus per maand
- `verhaal.html` — hetzelfde fictieve klantproject (Mira, De Schakel) verteld in as-is naast to-be, met vergelijkingsbord en agency-consequenties (Bain-synthese)
- `proces.html` — het volledige ontwikkelproces van A tot Z: zes principes, twee lussen (kwartaal + story-loop), vijf poorten, rollenbord (bestaat de FA nog?) en skills per rol
- `CLAUDE.md` — dit bestand. De methodologie compact opgeschreven.

Live op: https://antonaerts1-sys.github.io/functionele-analyse-2026/

## De methodologie in één paragraaf

Geen fases meer en geen handovers. Eén continue loop tussen discovery en delivery, met een product trio (PM, designer, engineer) in het midden, één meetbare outcome bovenaan, een AI-laag met MCP als ruggengraat eronder, en de klant wekelijks verbonden. Geen 80-pagina FAD-document, wel een werkend prototype dat de spec is. Geen kickoff-en-stilte, wel een wekelijks gesprek. Geen AI als losse experimentele tool, wel AI als structurele plumbing.

## De vier elementen

### 1. Het trio in het midden
- PM, designer, engineer als kleinste cross-functional unit
- Geen rolwissels, samen beslissen in gesprek van 30 min
- Bij kleinere teams: één T-shaped product engineer met alle drie de petten
- Stable unit over meerdere kwartalen voor compounding context

### 2. De continue loop
- Discovery en delivery lopen continu naast elkaar
- Geen begin, geen einde, alleen iteraties
- Vier vaste checkpoints op de loop (zie hieronder)

### 3. De outcome bovenaan
- Eén meetbaar business resultaat per kwartaal
- Niet een featurelijst, wel een KPI (conversie, retentie, adoptie, kostenbesparing)
- Continu gemeten, dashboard zichtbaar voor heel het trio
- Geen outcome = geen project

### 4. De AI-laag onder
- Structureel, geen losse experimenten
- MCP (Model Context Protocol) verbindt Linear, Figma, Cursor, Claude
- Achtergrondservice: het trio merkt AI niet als ze werkt
- Voorwaarde: domeincontext expliciet opgeschreven, anders fantaseert AI

## De vier checkpoints op de loop

| Checkpoint | Wanneer | Duur | Wie | Wat |
|---|---|---|---|---|
| Opportunity check | Wekelijks | 30 min | Trio | Opportunity solution tree updaten, beslissen welke story builden |
| Prototype walkthrough | Wekelijks | 30 min | Trio + klant | Klant test live prototype, designer past direct aan |
| Drift check | Per release | 15 min | Trio + AI | Code vergelijken met intent, afwijkingen bespreken voor release |
| Outcome review | Per kwartaal | 60 min | Trio + klant | Heeft KPI bewogen? Outcome voor volgend kwartaal vastleggen |

## Wat verdwijnt

- Lineaire fases (analyse → design → dev)
- Hand-over van document naar volgende persoon
- 60-pagina FAD die niemand teruglezt
- Wireframes als statisch tussenartefact
- Kickoff-en-dan-stilte met de klant
- AI als losse experimentele tool
- Featurelijst zonder gekoppelde KPI
- UAT-moment dat zes maanden te laat komt

## Wat in de plaats komt

- Continue loop tussen discovery en delivery
- Gedeeld werkend prototype als single source of truth
- Live opportunity solution tree (Vistaly, Mural, eigen tool)
- Wekelijks klantgesprek als ritme
- AI als structurele plumbing onder alles
- Eén meetbare outcome per kwartaal
- Drift check als release-ritueel
- Test suite als levend contract

## Wat je nodig hebt — vier lagen

### Laag 1 — Mensen
- PM met outcome-denken en JTBD-skill (jobs-to-be-done)
- Designer die prototypes bouwt, geen statische mockups
- Senior engineer met domeinkennis
- Optioneel: parttime domeinexpert in het trio
- Allemaal AI-geletterd: prompting, weten wanneer AI faalt, kritisch lezen

### Laag 2 — Rituelen
- Wekelijks klantinterview (Torres-style continuous discovery, 1 uur)
- Wekelijkse opportunity check (30 min trio sync)
- Drift check per release (15 min AI-assisted)
- Outcome review per kwartaal (60 min met klant)
- Shared workspace continu (Linear of Notion), geen mailthreads

### Laag 3 — Tools
- Discovery: Granola of Fathom (interviews), Vistaly of Mural (opportunity trees), Dovetail of Notably (research repo)
- Issue hub: Linear met agents (of Jira via MCP)
- Prototype: Figma Make, v0, Lovable, Claude Artifacts
- Code: Cursor of Claude Code
- Integratie: MCP als backbone
- Meting: DX Core 4 dashboard (Speed, Effectiveness, Quality, Business Impact)

### Laag 4 — Fundament
- Contract dat continuous discovery toelaat (geen fixed-scope fixed-price, eerder T&M of outcome-based)
- Enterprise AI-licenties, geen gratis tier met klantdata
- Privacy-architectuur met DPA's getekend per leverancier
- Toestemmingsflow voor opnames en transcripties standaard in elk klantgesprek
- Security review op MCP-connecties (welke tool ziet welke data)
- Eigenaar voor AI-geletterdheid binnen team (training, niet eenmalig)

## Pitfalls om te vermijden

### Tools-pitfalls
1. **AI zonder domeincontext** — levert hallucinaties op in specialistische domeinen. Schrijf domein expliciet op (2 A4 volstaat).
2. **MCP zonder governance** — connecties tussen tools moeten gereviewd worden op privacy en security.
3. **Gratis AI-tier met klantdata** — vogelvrij. Altijd enterprise, altijd DPA.

### Proces-pitfalls
4. **Outcome wordt featurelijst** — als je "outcome" hoort en het is een lijst van 5 dingen om te bouwen, herstart. Eén KPI.
5. **Trio verbreken** — als rolwissels weer ontstaan (analist schrijft, dev bouwt later), is het model gebroken.
6. **Klant niet in de loop** — wekelijks contact is het ritme, niet optioneel.

### Meet-pitfalls
7. **DORA als enige metric** — onvoldoende sinds AI-augmentatie. Gebruik DX Core 4.
8. **AI-perceptiegap** — devs voelen zich 20% sneller met AI maar zijn op grote codebases 19% trager (METR RCT, juli 2025). Meet uitkomst, niet sentiment.
9. **Drift onopgemerkt laten** — zonder structurele drift-check loopt productiecode weg van intent.

### Mens-pitfalls
10. **AI-geletterdheid als eenmalige cursus** — verouderd binnen 6 maanden. Continue training nodig.
11. **AI vertrouwen zonder verificatie** — AI is overtuigend ook als ze fout zit. Altijd zelf bronnen openen.

## Hoe pas je dit toe in een nieuw project

1. **Start met de outcome.** Geen brief, geen lijst, één KPI. Met de klant samen geformuleerd.
2. **Stel het trio samen.** Drie mensen, vaste samenstelling, vanaf dag één.
3. **Plan de eerste klantinterview voor week 1.** Niet "we doen eerst discovery", maar gesprek 1 op de kalender.
4. **Zet de AI-stack op.** Granola of equivalent, Linear, Figma Make, Cursor, MCP-connecties. Domein-context document.
5. **Definieer de vier checkpoints in de agenda.** Wekelijkse opportunity check, wekelijkse prototype walkthrough, drift check per release, kwartaalse outcome review.
6. **Begin parallel discovery + delivery vanaf week 2.** Niet eerst alles ontdekken, dan bouwen. Vanaf dag één samen.

## Bronnen achter deze methodologie

Deze doc is een synthese van een deep-research (juni 2026) op:

- Marty Cagan, *Transformed* (2024): Product Operating Model
- Teresa Torres, *Continuous Discovery Habits*: Opportunity Solution Tree, wekelijkse interviews
- Thoughtworks Haiven case (sept 2024): AI in requirements analysis, ~20% tijdwinst mits context
- Figma's "Prototypes are the new PRDs" (2025): ServiceNow, Ticketmaster cases
- Linear's AI agents en MCP-documentatie (2025-2026)
- DX Core 4 framework (jan 2025): vervangt DORA-only meting
- METR RCT (juli 2025): 19% slowdown voor ervaren devs met AI op grote codebases
- Craftzing Alivia case (2024-2025): multi-method discovery in Vlaamse healthcare context
- Pawel Huryn MCP demo (maart 2025): Figma + Atlassian + Claude integratie

Volledig rapport met 22 bronnen en 5 geweerde claims beschikbaar in vorige research-turn.

## Juridische onderbouwing bij het contractmodel (verhaal.html)

Het contractmodel in `verhaal.html` (vaste prijs in twee opties na de prototype-dag, klein genoeg voor een lichte gunning, daarna een kwartaalbedrag) steunt op deze Belgische regelgeving. Uitgezocht via deep-research juli 2026, adversarieel geverifieerd, geen juridisch advies.

### De 30.000 euro-drempel
Een overheidsopdracht met een geraamde waarde lager dan 30.000 euro excl. btw is een "opdracht van beperkte waarde". Die kan tot stand komen via een aanvaarde factuur: geen aankondiging, geen bestek, geen formele offerteaanvraag nodig. Bevestigd via de officiële bron: wet van 17 juni 2016 inzake overheidsopdrachten (hoofdstuk rond artikel 92), toegelicht op [FOD BOSA](https://bosa.belgium.be/nl/themas/overheids-opdrachten/marktkenniscentrum/overheidsopdrachten-van-beperkte-waarde-klassieke).

### Wanneer geldt dit voor een vzw: de functionele analyse (FA-test)
Een vzw is niet automatisch onderworpen aan de overheidsopdrachtenwet. Ze telt pas mee als "aanbestedende overheid" als cumulatief voldaan is aan drie voorwaarden:
1. Opgericht met het specifieke doel te voorzien in een behoefte van algemeen belang van niet-industriële of niet-commerciële aard
2. Rechtspersoonlijkheid
3. Overheidsafhankelijk: financiering in hoofdzaak door een overheid, of beheerstoezicht, of meer dan de helft van de bestuursleden aangewezen door een overheid

Voldoet een vzw aan alle drie, dan geldt de **infectietheorie**: één enkele activiteit van algemeen belang trekt de hele organisatie onder de wet, ook haar andere, zuiver private activiteiten.

Zelfs een vzw die zelf niet als aanbestedende overheid kwalificeert, kan voor één specifieke opdracht alsnog onder de wet vallen als die opdracht zwaar gesubsidieerd wordt door een aanbestedende overheid (cumulatieve voorwaarden rond het subsidiepercentage en het type werk).

### Praktisch voor Statik
- Bij een federale of overheidsklant (zoals CTRG) geldt de 30.000 euro-regel rechtstreeks en voorspelbaar
- Bij een "gewone" vzw zonder overheidsafhankelijkheid geldt de wet mogelijk helemaal niet: vrijer dan gedacht, geen beperking op de offerte
- Bij een zwaar gesubsidieerde of overheidsgestuurde vzw: vooraf checken via de FA-test of ze eronder valt. Valt ze eronder, dan blijft een project van 15.000 tot 30.000 euro nog steeds binnen het lichte aanvaarde-factuur-regime

### Wat nog niet onderzocht is
Doorlopende kwartaalfacturatie binnen subsidie-enveloppes (bouwsteen 6 van het onderzoek) is niet apart bronbevestigd. Dat blijft een logische afleiding, geen getoetst feit. Bij twijfel over een concreet geval: juridisch checken, dit is geen advocaat-advies.

## Maandritueel voor maandfocus.html

Alle inhoud van `maandfocus.html` staat in het `DATA`-object onderin dat bestand. Anton werkt dit maandelijks bij via Claude, nooit met de hand. Zo gaat dat:

1. Anton geeft de focus van de nieuwe maand en de acties per fase door.
2. Verplaats de acties van de aflopende maand naar `historiek` van de betreffende fase (nieuwste maand bovenaan), met hun `done`-status zoals ze eindigden.
3. Zet `maand` op de nieuwe maand, vul `focus` en de nieuwe `acties` in (`{ tekst: "…", done: false }`).
4. Tussendoor mag ook: een actie afvinken (`done: true`) of acties toevoegen binnen de lopende maand.
5. Commit en push naar `origin main`; GitHub Pages publiceert automatisch.

Skills per fase zijn stabieler; pas die alleen aan als Anton daarom vraagt.

## Versie en update-discipline

- Versie 1.0, juni 2026
- AI-tooling landschap beweegt snel. Herzie elke 3 maanden welke specifieke tools nog top zijn.
- Methodologie (4 elementen, 4 checkpoints, 4 lagen) is stabieler. Pas alleen aan als nieuwe research dit fundamenteel ondergraaft.
