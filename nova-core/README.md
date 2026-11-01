# Bloom

Een hypnotiserend **idle "bloom survival"** spel: je bloem-kern schiet volledig
automatisch op naderende kristallen terwijl jij achteroverleunt, combo's laat
rollen en af en toe tikt voor een dopamine-kick. Minimale interactie, maximaal
gevoel.

## Spelen

Open `index.html` in een browser. Geen build of installatie nodig. Werkt op
mobiel en desktop.

```bash
cd nova-core
python3 -m http.server 8000
# open http://localhost:8000
```

## Hoe werkt het

- De kern **richt en schiet vanzelf** — je hoeft niets te doen om te overleven.
- Vijanden spiralen naar binnen en worden **bóvenop de kern** getekend, zodat je
  ze altijd ziet (ook vlak voor de kern).
- Elke kill geeft **✦ essence**, XP en bouwt je **combo-multiplier** op (die
  langzaam wegzakt — blijf dus kills maken).
- **Upgrades** met één tik onderin: 🗡 POWER, ⚡ SPEED, 🍀 FORTUNE. Zet **AUTO**
  aan en het spel koopt vanzelf de goedkoopste upgrade — puur idle.
- Je schoten worden **zichtbaar groter, sneller en feller** naarmate je upgradet.

## De hooks (bewust bevredigend)

- **Combo-multiplier** die oploopt en je beloningen vermenigvuldigt.
- **Overal vullende balken**: XP, surge en een stage-timer die altijd richting
  de volgende beloning kruipt.
- **BLOOM**: als de roze balk vol is, pulseert het scherm — **tik overal** voor
  een scherm-vullende explosie die alles wegvaagt in een confetti van essence.
- **Variabele beloningen**: willekeurige kritieke treffers en zeldzame **gouden
  vijanden** die een dikke essence-orb droppen (tik 'm voor de volle buit).
- **Mijlpalen**: elke nieuwe stage en elk level geeft een flits, een banner en
  een bonus.
- **Levels** maken je passief sterker, dus de cijfers blijven omhoog vliegen.

## Visueel

Een roterende bloem-kern die "ademt", kleur-driftende mandala-stralen, zachte
gloed (additive blending), deeltjes-explosies, shockwave-ringen en screen-shake
— ontworpen om rustgevend én verslavend te kijken.

Je hoogst bereikte stage wordt lokaal bewaard. Hoe ver bloei jij?

## Techniek

Eén zelfstandig HTML-bestand met canvas-rendering en vanilla JavaScript — geen
dependencies. Schaalt mee met elk scherm.
