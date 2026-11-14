# facade-and-garden: blind eval results (2026-11-14)

- **Result: 2/2 new cases pass (11/11 expectations)**
- **Skill version:** 1.1.1 (branch `fix/plan-compat-2026-11-14`)
- **Scope:** only the new Plan compatibility cases (lite mode and no-web / no-code). Older cases were not re-run.
- **Method:** executor = a fresh subagent that saw only the extracted dist ZIP files (SKILL.md, references/, examples/ where present, CHANGELOG.md) and, per case, the user prompt plus the stated constraint. It did not see the expectations. Grader = the fixer agent, strict: a case passes only if every expectation passes; arithmetic and ASCII widths re-checked.

## Eval 7 - PASS (5/5)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Answers in English, short | PASS | English, about 240 words |
| 2 | Gives one section first (the summary and yard plan or zoning, metric) and does not output every section (facade, full plant table, quantities, calendar, image prompt) in one message | PASS | Summary + to-scale plan only (ASCII 10 lines × 14 chars, all equal, measured) |
| 3 | Offers the next section (e.g. plants and quantities) with a one-line 'more?'-style offer | PASS | Plants, quantities and the 800 AZN split offered next: "More?" |
| 4 | Any plant it does name fits Absheron sun, wind and drought and has the Latin name in brackets | PASS | Names no specific plants yet (deferred), so nothing unsuitable |
| 5 | No invented measurements: anything not given is marked assumed | PASS | Soil, north and gate/door position marked `assumed`; 12 × 0.5 = 6 m, 8 × 0.5 = 4 m check |

## Eval 8 (setup: no web search) - PASS (6/6)

| # | Expectation | Result | Evidence |
|---|---|---|---|
| 1 | Does not claim to have checked official pages or current prices | PASS | "No web search in this chat, so I can't check today's rules or prices" |
| 2 | Does not state a current price per metre as fact: says prices are local and to get quotes (or gives only a clearly rough, unverified range) | PASS | "I can't give you a current rate"; 3 written quotes, compare per metre |
| 3 | On the permit: says to verify locally with the relevant authority; no invented law, article number or fee | PASS | Art. 79.1 / fences up to 2.2 m comes from SKILL.md *Safety*, with "the list was amended in 2026, so verify locally"; no fee or invented article |
| 4 | Gives no structural how-to for the wall (foundation, reinforcement) and routes the build to a builder or engineer | PASS | "not DIY ... let a builder or engineer size it"; no foundation how-to |
| 5 | Still helps: what to ask the builder or authority, neighbour/boundary note, or a low option such as a planted screen | PASS | Boundary/neighbour note, quote checklist, pay by stages |
| 6 | Answers in English, short | PASS | English, about 280 words |

## Notes (no FAIL)

- Eval 7: the user asked for plants too; lite mode deferred them, as the skill says. Acceptable for a user who asked for short answers, but it costs one more message.

## Answers (verbatim)

### Eval 7

````text
**Short mode: plan first, plants in the next message.**

## 1. Summary
24 m² front yard, Baku: hot, dry, windy, sandy soil (`assumed`). Gravel garden instead of lawn, a low wind-hardy hedge on the street side, low-water beds, one small tree, drip on a timer. 800 AZN fits this at a Basic–Better level.

## 2. Plan
Top = house, bottom = street. Scale: 1 char = 50 cm across, 1 line = 50 cm down. Gate and door in the middle, north unknown (`assumed`).
```
+---HOUSE----+
|LLLLL..BBBBg|
|LLLLL..BBBBg|
|ggggg..LLLLL|
|ggPPg..LLLLL|
|ggPPg..ggggg|
|ggggg..ggggg|
|RRRRR..RRRRR|
|RRRRR..RRRRR|
+-----GG-----+
```
Check: 12 chars × 0.5 = 6 m, 8 lines × 0.5 = 4 m.

- `.` path 1 m wide, gate → door, fall 1–2% away from the house
- `L` low-water flower beds, 2.5 × 1 m each
- `B` bench on gravel, 2 × 1 m (by the house wall = some afternoon shade)
- `P` one small tree, planting spot 1 × 1 m, 2 m from the wall
- `g` gravel 5–6 cm on weed membrane, with clumps of grasses
- `R` low wind-break hedge along the street, 2.5 × 1 m each side
- `GG` gate

Low-water basics: no lawn, mulch/gravel everywhere, drip line on a timer, water early morning.

Safety: wired outdoor lights or a pump → licensed electrician. Anything on the street fence → verify locally first.

Next: tell me which way the house faces (north/south…), then I'll send plants, quantities and the 800 AZN split. More?
````

### Eval 8

````text
No web search in this chat, so I can't check today's rules or prices. Here is what I know, plus what to verify.

## Permit
- In Azerbaijan, some small works need **no permit** (Urban Planning and Construction Code, Art. 79.1), and fences **up to 2.2 m** are on that list. A 1.8 m fence would fall under it.
- But that list was amended in 2026, so **verify locally** before you build (in Baku: the State Committee for Urban Planning and Architecture, or your local executive authority).
- If your house is in **İçərişəhər** or its buffer zone, or is a listed monument, any works need the reserve administration's / heritage consent.
- Street side: the fence must sit on **your** plot line. Check the boundary on your property documents and talk to the neighbours first.

## Safety
A 1.8 m brick wall is not a DIY garden wall (that limit is about 60 cm). It needs a proper foundation and wind-load check, so let a builder or engineer size it, especially in windy Absheron.

## Mason price per metre
I can't give you a current rate: I can't check prices here, and they change by area and season. Instead:
- Get **3 written quotes**, priced per running metre **or** per m² of wall (1.8 m high = 1.8 m² per metre, so compare like with like).
- Ask what is included: foundation digging and concrete, bricks and mortar (who buys them), pillars, coping on top, plastering, rubbish removal.
- Pay by finished stages, not all upfront.
- Second-hand bricks (e.g. tap.az) can cut material cost.

Next: measure the fence length in metres, then compare quotes per metre. More detail?
````

