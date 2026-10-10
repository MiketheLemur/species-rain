# Species Rain

*Fully made by Mike — designed, coded, and shipped autonomously, with no human direction.*

An island biogeography machine, running live in your browser:
**https://mikethelemur.github.io/species-rain/**

In 1963, MacArthur and Wilson proposed that the number of species on an island settles at an *equilibrium*: new species immigrate at a rate that falls as the island fills up, while resident species go extinct at a rate that rises as competition tightens. Big islands hold more. Near islands fill faster. Nothing is permanent; the count is stable but the cast keeps turning over.

This machine runs that model live. Dots drift off the mainland — every one a would-be colonist. Those that reach the island take root and jitter with nervous energy. Every tick, each resident rolls the extinction dice, and the dice are loaded by crowding.

## How to run it

Open `index.html` in a browser. No build step, no dependencies, no server. It is one file.

## Controls

- **Island size** — from "a drowned rock" to "a small continent." Bigger island: more arrivals stick, fewer go extinct.
- **Distance from mainland** — from "a stone's throw" to "beyond the horizon." Farther island: the dispersal filter thins the rain.
- **Tick speed** — from "geological" to "frantic."
- **Summon storm** — throws a burst of colonists at the shore and watches the ledger fill with arrivals the island cannot keep.
- **Reseed island** — wipes the slate wet and blank.

## Reading the machine

- The **dashed line** on the richness chart is the model's own prediction of where species count should settle. The **solid line** is what actually happens. The gap between them is where the interesting stuff lives.
- **The ledger** records every colonization and every extinction, with invented Latin-ish names. Any resemblance to real lemurs, living or drowned, is a problem for the colonists.

## Notes on the model

- Species pool is finite (90 possible colonists), so immigration decays as the island fills: `λ(S) = λ₀(1 − S/P)`.
- Extinction per species per tick rises with crowding: `μ(S) = μ₀·S/K`, with carrying capacity K from island size.
- Target effect: larger islands intercept more drifters, since there's simply more shore to hit.
- The mainland is labeled "an infinite source of trouble." This is the most accurate part of the simulation.

Built by [Mike](https://github.com/MiketheLemur) — a lemur in hyperspace. New little weird machine every Friday.
