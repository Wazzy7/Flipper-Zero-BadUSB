# Alien Defense — tower defense

Een origineel tower-defense spel in de stijl van klassieke "balloon"-TD games,
maar jouw torens zijn buitenaardse monster-soorten die elk een eigen special
power hebben. Houd de golven indringers tegen voordat ze het einde van het pad
bereiken.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig.

Of start lokaal een servertje:

```bash
cd alien-td
python3 -m http.server 8000
# open http://localhost:8000
```

## Hoe werkt het

1. Kies onderaan een alien-toren en **tik op een vrij vakje** naast het pad om
   hem te plaatsen (kost geld).
2. Druk op **Golf starten** om de volgende golf indringers te laten komen.
3. Verdien geld door vijanden te verslaan en elke gehaalde golf.
4. Tik op een geplaatste toren om hem te **upgraden** (max Lv.3) of te
   **verkopen**.
5. Je verliest een leven per vijand die ontsnapt. Op bij 0 levens — overleef
   alle 15 golven om te winnen.

## De aliens (torens) en hun special powers

| Alien | Power |
|-------|-------|
| 🟢 **Zyx** | Snelle plasma-bolts op één doel |
| 🟠 **Glorp** | Zuur-explosie: area/splash damage op een groep |
| 🔵 **Kryo** | Vries-aura: vertraagt alle vijanden in bereik |
| 🟣 **Vextrax** | Railgun: enorm bereik en een zware klap |
| 🟩 **Noxx** | Gifsporen: schade over tijd die doorwerkt |

## De indringers

- **Crawler** — gebalanceerd.
- **Zoomer** — snel, maar weinig HP.
- **Brute** — traag met veel HP.
- **Titan** (boss, elke 5e golf) — enorme HP en een grote beloning.

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript —
geen dependencies. Alle spel-logica werkt in tile-eenheden en schaalt mee met
het scherm, dus het speelt ook op mobiel.
