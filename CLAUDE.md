# Lunchrad

## Wat is dit
"Lunch van de Maand", een draairad voor The Kind Kids dat bepaalt wie de lunch verzorgt (of wint). Eén statische `index.html` met een canvas-rad met een namenlijst (45 deelnemers sinds 21 augustus 2026), tick-geluiden, pointer bounce, dramatische easing en fullscreen-reveal. Twee spins per trekking; de tweede spin kan niet op een al geëlimineerde persoon landen (fair randomness, zie git log).

## Stack
Statische HTML, geen build, geen dependencies. GT Flexa-fonts (TKK-huisstijl) en het TKK-logo zitten als base64/inline SVG in het bestand, geen externe requests.

## Deployment
GitHub Pages workflow in `.github/` (sinds 31 maart 2026).

## Starten
Open `index.html` in de browser.

## Staat
- Werkend, gebruikt eindproduct, geen experiment.
- Tandwiel rechtsboven: afwezigen afvinken, bewaard in localStorage (`lunchrad-afwezig`). Confetti bij de finale = dwarrelende TKK-logo's in de merkkleuren (gegenereerd uit het inline SVG). Geluid: tik bij draaien, casino-belletjes per winnaar, koor "aaah" gevolgd door trompetfanfare bij de finale (alles Web Audio, geen bestanden).
- Laatst bijgewerkt 21 augustus 2026 (45 namen, huisstijl, geluid, aanwezigheidspaneel). Namen bijwerken gebeurt rechtstreeks in `index.html`.
- Er bestaat ook `tkk-rad/`, een veel uitgebreidere Next.js-versie van hetzelfde idee.
