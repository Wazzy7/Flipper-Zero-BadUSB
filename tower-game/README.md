# The Tower — stapelspel

Een simpel, origineel stapelspel in de stijl van klassieke "tower"-games. Laat
blokken vallen en stapel ze zo precies mogelijk op elkaar. Alles wat uitsteekt
valt eraf en maakt de toren smaller — hoe hoger je komt, hoe sneller het gaat.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig.

Of start lokaal een servertje:

```bash
cd tower-game
python3 -m http.server 8000
# open http://localhost:8000
```

## Besturing

- **Tik** op het scherm, of druk op **spatie** / **pijl omlaag** / **enter**
  om het bewegende blok te laten vallen.
- Een perfecte landing (netjes uitgelijnd) laat de toren níét krimpen.
- De game eindigt zodra een blok volledig naast de toren valt.

Je hoogste score (aantal verdiepingen) wordt lokaal in de browser bewaard.

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript —
geen dependencies.
