# Facade and Garden

> Describe your house, plot, climate and budget. Get facade options with materials and hex colours, a zoned garden plan in ASCII, plants that fit your climate with mature sizes, path and step sizes, a low-water option, a phased budget, a care calendar and a prompt to visualise it with free image tools.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757.svg)](SKILL.md)
[![Price: Free](https://img.shields.io/badge/price-free-brightgreen.svg)](#license)

A free, text-only skill by Codelady Abroad for first-time house and dacha owners and anyone with a small yard. It runs anywhere a plain prompt runs: Claude Code, the Claude app, other agents or a website form. No scripts, files or paid tools.

## What you get

- Up to 6 short questions, only for what is missing.
- Three facade options: material pairs, climate fit, maintenance, cost level.
- Three exterior colour schemes with hex codes (walls, base, trim, door, roof).
- Garden zoning (entry, sitting, play, utility, growing) with a to-scale ASCII plan.
- Plant table by zone with Latin names, sun, water, mature size, and toxic-plant warnings.
- Path, terrace and step sizes with the 2 × rise + tread comfort check and drainage falls.
- Low-water garden option for dry climates such as Absheron.
- Outdoor lighting, a phased shopping list by budget level with contingency, and a seasonal care calendar.
- An image prompt for before/after concepts and free tools to try.
- Answers in the user's language.

## Safety

Structural work, retaining walls, outdoor electrics, gas, drains, big trees and permits (including heritage zones) go to a licensed professional. The skill says so plainly and gives no how-to steps for them.

## Example request

> I have a one-storey brick house near Baku (Mardakan). The yard is 12 × 15 m, the front faces south, it is very windy and we have limited water. I want a shady place to sit in the evening, a small vegetable corner and something nicer than the grey facade. Budget about 4000 AZN.

## Install

- **Claude Code:** copy this folder to `~/.claude/skills/facade-and-garden/`.
- **Claude app:** zip the folder (with `SKILL.md` inside `facade-and-garden/`) and upload it under *Customize → Skills*.
- **Any other agent or a web form:** use the body of `SKILL.md` as the system prompt. `references/` holds optional tables.

Test prompts and expected points: [`evals/evals.json`](evals/evals.json).

## Sources and credits

Written from scratch. Values are rounded good practice, informed by:
- RHS Plant Finder (plant sizes, sun and soil needs)
- Köppen climate classification and USDA hardiness zones
- Neufert, *Architects' Data* (paths, steps, the Blondel step rule)
- ADA 2010 Standards (ramp slope and landings)
- Local planning and heritage rules (to be verified locally)
- The gap analysis in Codelady Abroad's own research notes; the idea of a yard-planning skill also appears in curiositech's `fancy-yard-landscaper` (no text was taken from it).

Confirm plants with a local nursery and building work with a licensed builder.

## License

[MIT](LICENSE) © 2026 Codelady Abroad
