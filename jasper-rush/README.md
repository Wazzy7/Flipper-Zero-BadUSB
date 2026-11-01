# Jasper Rush

Een origineel, kleurrijk match-3 snoep-puzzelspel in de "juicy" visuele stijl
van candy-games — met glanzende snoepjes, deeltjes-explosies, screen-shake, een
animerende achtergrond met zwevende sprinkles en oplopende **cel-multipliers
(×2 → ×128)**. De ster van de show is een speciale **Jasper-tegel** die een
"JASPER RUSH!" bonus triggert.

> Dit is een puzzel-/behendigheidsspel om punten te scoren — geen gok- of
> casinospel. Alleen de vrolijke visuele stijl is overgenomen.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig. Alles zit in
één bestand (Jaspers foto is ingebed), dus het werkt ook op mobiel en via een
preview-link.

Of start lokaal een servertje:

```bash
cd jasper-rush
python3 -m http.server 8000
# open http://localhost:8000
```

## Hoe werkt het

- **Veeg of tik** twee aangrenzende snoepjes om ze te ruilen. Een ruil mag
  alleen als er een rij van **3 of meer** gelijke snoepjes ontstaat.
- Geruimde snoepjes vallen weg, nieuwe vallen erin — **ketting-combo's** geven
  steeds meer punten.
- Elk vakje dat knalt krijgt een **multiplier** die verdubbelt (×2 → ×128). Op
  dezelfde plek blijven knallen = enorme scores.
- **5 op een rij** laat een **Jasper-tegel** verschijnen (en soms valt er
  spontaan eentje binnen).
- **Tik op een Jasper-tegel** om een kruis (hele rij + kolom) weg te blazen:
  **JASPER RUSH!** — met een grote animatie van Jasper zelf.
- Haal de **doelscore** binnen je aantal zetten om naar het volgende level te
  gaan. Elk level heeft een hogere doelscore en iets meer zetten. Raak je
  zonder het doel te halen door je zetten heen, dan is het game over. Je
  topscore wordt lokaal bewaard.

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. De afbeelding van Jasper is als data-URI ingebed. Alle spel-logica
schaalt mee met het scherm, dus het speelt ook prettig op mobiel.
