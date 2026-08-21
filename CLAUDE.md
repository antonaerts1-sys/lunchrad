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
- Draaien gaat via de gokkast-hendel rechts van het rad (slepen of klikken, pointer events), knop = TKK-hartje; de oude knop is een tekst-hint. Kermisboodschappen ("Altijd prijs", ...) flitsen in de witte marge naast het rad, enkel op het beginscherm en vanaf 900px breed. Tandwiel rechtsboven: afwezigen afvinken, bewaard in localStorage (`lunchrad-afwezig`). Slotscherm = vol blauw TKK-vlak met enkel logo, namen in condensed, &-sticker en pill-knop (geen losse artefacten, Anton 21/08). Confetti = 14 s regen van logo's + kribbels; bloemenregen bij winnaar 1, hartjesregen bij winnaar 2. Muisspoor = enkel echte artefacten (kribbels, logo, pijl), geen bollen. Reviewkopie als Claude-artifact (comments daar): https://claude.ai/code/artifact/941624fd-fba6-4ce1-9569-5be5f8e9eee2 Rad schaalt mee met breedte en hoogte (`--wheel`, max 520px). Titel staat als draaiende tekstring rond het rad, logo in de footer. TKK-kribbels (hart, sterren, bloem, zon...) uit tkk-kaartjesmaker/kribbels zitten inline (`KRIBBELS`) en worden gebruikt in muisspoor, confetti en slotscherm. Geluid: tik bij draaien, casino-belletjes per winnaar, koor "aaah" gevolgd door trompetfanfare bij de finale (alles Web Audio, geen bestanden).
- Laatst bijgewerkt 21 augustus 2026 (45 namen, huisstijl, geluid, aanwezigheidspaneel). Namen bijwerken gebeurt rechtstreeks in `index.html`.
- Er bestaat ook `tkk-rad/`, een veel uitgebreidere Next.js-versie van hetzelfde idee.
