# Nova Core

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
- Spendeer cash aan upgrades in drie tabbladen:
  - ⚔ **Aanval** — schade, vuursnelheid, bereik, meervoudig schot, kritiek
  - 🛡 **Verdediging** — max leven, regeneratie, pantser, schokgolf
  - ★ **Economie** — cash-bonus per kill, cash per golf, rente op je cash
- Elke **10e golf** komt er een **boss** met veel leven en een grote beloning.
- Versnel het spel met de **snelheidsknop** (×1 / ×2 / ×4).

Golven worden steeds groter en sterker. Je hoogst bereikte golf wordt lokaal
bewaard. Hoe ver kom jij?

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. Alle arena-logica werkt in schaal-onafhankelijke coördinaten, dus
het speelt op elk scherm.
