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
## Power-ups

Bepaalde combinaties maken een speciale tegel die op het bord blijft staan. Tik
erop om 'm af te vuren — power-ups **ketting-reageren** door elkaar heen voor
enorme combo's:

- **4 op een rij** → **streep-snoep**: blaast de hele rij (horizontaal) of kolom
  (verticaal) weg, met een lichtstraal.
- **Kruis / L-vorm** (horizontaal + verticaal tegelijk) → **bom**: 3×3 explosie
  met een shockwave.
- **5 op een rij** → **Jasper-tegel**: blaast rij + kolom weg met de grote
  **JASPER RUSH!**-animatie van Jasper zelf.

Je kunt een power-up ook activeren door 'm in een gewone match mee te nemen.

## Levels

- Elk level moet je de **doelscore** halen binnen je aantal zetten. De
  levelscore begint elk level weer op **0**, dus je moet het doel telkens
  opnieuw verdienen — en het doel groeit elk level (×1,5: 1.200 → 1.800 →
  2.700 → …), terwijl je er maar iets meer zetten bij krijgt. Zo wordt het
  level na level moeilijker.
- Lukt het, dan verschijnt een **level-voltooid-scherm** met een
  **zetten-bonus** (overgebleven zetten leveren extra punten op), je
  **totaalscore** en het volgende doel.
- Raak je zonder het doel te halen door je zetten heen, dan is het game over.
  Je **totaalscore** over alle levels telt, en je topscore wordt lokaal
  bewaard.

## Visuele effecten

Glanzende snoepvormen, deeltjes-explosies met sterretjes, screen-shake,
lichtstralen (beams) bij streep-snoep, shockwaves bij bommen, een witte flits bij
grote scores, combo-popups, oplopende multiplier-labels, confetti bij een
level-up, en een animerende candy-lucht met zwevende sprinkles.

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. De afbeelding van Jasper is als data-URI ingebed. Alle spel-logica
schaalt mee met het scherm, dus het speelt ook prettig op mobiel.
