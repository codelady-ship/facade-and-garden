# Changelog

All notable changes to this project are documented here.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and the project uses [Semantic Versioning](https://semver.org/).

## [1.1.0] - 2026-11-11

Research-driven features before the Agensi listing (open-skills research, 2026-11-11).

### Added
- `references/garden-care-and-quantities.md`:
  - **Vegetable sowing calendar** per Azerbaijani region (marked approximate).
  - **Companion planting and a 4-group rotation**.
  - **Pest and disease first aid** from a description, least-toxic fix first.
  - **Soil fixes** for sandy, salty and clay soil.
  - **Watering amounts, drip run-time formula** and rain-tank sizing.
  - **Material quantities:** gravel/mulch m³ and tonnes, pavers, edging, plant count.
  - **Balcony container garden** with a weight and wind warning.
  - **Privacy screen** options by speed and cost.
- Plant tables get a **kids/pets toxicity column**; toxic plants are never placed by play areas.
- `examples/sevda-absheron-yard-with-kids.md`.
- Agensi frontmatter (`version`, `summary`, `tags`, `keywords`, `use_cases`), `scripts/build-agensi-zip.ps1`, `LISTING.md`, evals 4–6 and blind test results in `tests/`.

### Fixed (checked on official pages, 2026-11-11)
- Toxicity: oleander, English ivy, hydrangea and boxwood are toxic to dogs and cats (ASPCA); boxwood is low-toxicity for people.
- Azerbaijani permits: İçərişəhər reserve consent; notification (not permit) for private houses up to 3 floors (Code Art. 80, 10-day rule); no-permit list in Art. 79.1 (fences up to 2.2 m, small sheds and greenhouses), marked as amended in 2026; Baku permits via the State Committee for Urban Planning and Architecture, elsewhere the local executive authority. Facade colour rules for Baku: none found, so the skill says "ask".

### Fixed (blind evals, 2026-11-11)
- Facade options use fixed labels, with a Care line for every option.
- ASCII plan caption and N↑ above the code block; rows × scale must equal the real size.
- After a safety refusal (retaining walls, heavy cladding) the answer still gives the safe part: plants, drainage away from the house, seasonal calendar.
- Toxicity flags for male fern and hosta.

## [1.0.0] - 2026-11-10

### Added
- First release: facade options and colour schemes with hex codes, garden zoning with an ASCII plan, plant lists by climate, hardscape sizes, low-water option, outdoor lighting, phased budget, care calendar, image prompt, safety routing. MIT.
