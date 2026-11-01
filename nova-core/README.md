# Nova Seed (Nova Core)

Een origineel idle/round-based tower-survival spel in een bekend genre: een
centrale kern die automatisch op naderende vijanden schiet terwijl jij 'm
versterkt met upgrades. Eigen visuele stijl (gloeiende plasma-kern met
roterende ringen, kristal-vijanden, warm paars/amber thema), eigen upgrades en
balans — geen kopie van een bestaand spel.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig. Werkt ook op
mobiel/tablet.

```bash
cd nova-core
python3 -m http.server 8000
# open http://localhost:8000
```

## Hoe werkt het

- Je **kern** staat in het midden en **schiet automatisch** op het dichtstbijzijnde
  kristal binnen bereik. Jij hoeft alleen te upgraden.
- Vijanden komen van de randen naar binnen. Bereiken ze de kern, dan verlies je
  leven. Op 0 leven is het game over.
- Verslagen vijanden geven **cash**; elke gehaalde golf geeft bonus + rente.
- Spendeer cash aan upgrades in vier tabbladen:
  - ⚔ **Aanval** — schade, vuursnelheid, bereik, meervoudig schot, kritiek
  - 🛡 **Defensie** — max leven, regeneratie, pantser, schokgolf
  - ★ **Economie** — cash-bonus, cash per golf, rente, XP-bonus
  - 🌱 **Gadgets** — krachtige modules die vrijkomen naarmate je levelt
- Je schoten worden **zichtbaar sneller, groter en feller** naarmate je upgrades
  koopt.
- Elke **10e golf** komt er een **boss** met veel leven en een grote beloning.
- Versnel het spel met de **snelheidsknop** (×1 / ×2 / ×4).

## XP, levels en gadgets

- Verslagen vijanden en gehaalde golven geven **XP**. Vol = **level up**: je
  wordt passief sterker én krijgt een **✦ gadget-punt**.
- Spendeer gadget-punten in de **Gadgets**-tab. Elke gadget komt vrij vanaf een
  bepaald level:
  - 💰 **Gouden oogst** — meer cash + XP per kill (Lv.1)
  - ❄️ **Vorstveld** — vertraagt vijanden in bereik (Lv.2)
  - 🌱 **Spruit-drones** — orbitale spruiten die mee schieten (Lv.3)
  - ⚡ **Kettingschok** — schoten springen over naar extra vijanden (Lv.4)
  - 🔥 **Brandzaad** — schoten zetten vijanden in brand (Lv.5)

## Zaad-thema

De kern is een **groeiend zaad**: naarmate je levelt lopen er blaadjes uit.
Een duidelijke **bereik-zone** laat precies zien waarop de kern kan schieten, en
een **golf-voortgangsbalk** toont hoe ver je in de golf bent en hoeveel vijanden
er nog zijn.

Golven worden steeds groter en sterker. Je hoogst bereikte golf wordt lokaal
bewaard. Hoe ver kom jij?

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. Alle arena-logica werkt in schaal-onafhankelijke coördinaten, dus
het speelt op elk scherm.
