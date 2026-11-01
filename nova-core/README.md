# Bloom Defense

Een originele **idle tower-defense** in de stijl van het genre (centrale kern die
automatisch golven afweert terwijl je stats upgradet), met een eigen
hypnotische bloem-look. Geen kopie van een bestaand spel — eigen visuals,
naamgeving en balans.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig. Werkt op
mobiel, tablet en desktop.

```bash
cd nova-core && python3 -m http.server 8000   # → http://localhost:8000
```

## Opzet

- **Golven** met zichtbare vijand-stats (❤ HP en ⚔ schade) en een
  voortgangsbalk; elke **10e golf** is een **boss** die 💎 gems dropt.
- Een prominente **kern-HP-balk** en een HP-ring rond de bloem.
- **Snelheidsregelaar** (− / ×N / +) van ×1 t/m ×4.
- **AUTO-KOOP** die automatisch de goedkoopste upgrade koopt — puur idle.
- **BLOOM-ultimate**: als de roze balk vol is, tik overal voor een
  scherm-vullende explosie.
- Combo-multiplier, crits, gem-drops en juice voor dat "cijfers omhoog"-gevoel.

## Upgrades (4 tabbladen)

- ⚔ **Aanval** — schade, vuursnelheid, kritiek kans, kritiek factor, bereik,
  multishot
- 🛡 **Defensie** — max leven, regen, pantser, doornen
- ★ **Utility** — cash-bonus, cash/golf, rente, gem-kans
- 🌸 **Ultimate** (met 💎 gems) — spruit-drones, kettingschok, brandzaad,
  vorstveld

Cash koop je met (uit kills + golf-bonus + rente); gems verdien je van bosses en
een upgradebare gem-kans, en geef je uit aan de krachtige Ultimate-gadgets.

Je hoogst bereikte golf wordt lokaal bewaard. Hoe ver kom jij?

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. Schaalt mee met elk scherm.
