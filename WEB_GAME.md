# Xuantian World — Web RPG Prototype

Playable single-player browser prototype inspired by the *cultivation sandbox/RPG* feel of games such as Tale of Immortal, while using original Xuantian World names, rules, locations, factions and formulas from this repository.

## Current systems

- Character creation: name, Spiritual Root, profession, starting Zhou.
- 9 Xuantian cultivation realms × Early/Mid/Peak stages.
- Qi Cap and breakthrough chances based on `13_SPIRITUAL_ROOT_SYSTEM.md`.
- HP, Stamina and Satiety based on `16_VITALITY_HUNGER_SYSTEM.md`.
- Turn-based combat, initiative-style combat structure, attack/defense and hit logic based on `17_COMBAT_SYSTEM.md`.
- 10 Zhou map and regional travel.
- Mortal currency + Low-Grade Spirit Stone economy concepts from `15_ECONOMY_SYSTEM.md`.
- Exploration events, karma, loot, inventory and factions.
- Local save via browser `localStorage`.
- Mobile-first responsive UI; no external libraries or build step.

## Run locally

Open `index.html` in a modern browser. The game is a static HTML/JavaScript application.

## GitHub Pages

The branch includes `.github/workflows/pages.yml`. Enable GitHub Pages for the repository using **GitHub Actions** as the source. The workflow publishes the repository as a static site.

## Next development stage

1. Replace prototype combat with the full combat module implementation.
2. Load regional encounters, beasts, sects and professions from structured JSON generated from the World Bible.
3. Add procedural events from `41_CUSTOM_EVENTS.md`.
4. Add NPC relationships, quests, sect/preguruan progression and dynamic world simulation.
5. Add airship routes and the full dynamic-market formula.
6. Add a proper save-slot/export system.

This is a game implementation of the repository's lore, not a copy of Tale of Immortal's code, artwork or proprietary assets.
