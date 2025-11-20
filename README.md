# STATS 102A — HW4: Monopoly Simulation (R, OOP)

Simulate Monopoly turns with object-oriented R, validate behavior with fixed test cases, and estimate long-run landing frequencies via **1,000 simulated games**. Output includes verbose test traces and summary plots.

---

## Files
- `102a_hw_04_output_Daren_Sathasivam.pdf` — rendered output: printed traces for test cases, 1k-game results, and barplots. :contentReference[oaicite:1]{index=1}
- `102a_hw_04_output_Daren_Sathasivam.Rmd` — R Markdown source (analysis + code).

> Note: Some scaffolding references a separate script (e.g., `102a_hw_04_script_*.R`) that defines classes and helpers used by the Rmd. If you keep that file private (recommended), document the public API of the classes in the Rmd.

---

## What it does
- **OOP design**: `Player`, `SpaceTracker`, `CardDeck`, and `Dice` (preset and random) objects coordinate game state and turns.
- **Rules implemented**: doubles logic (3 doubles → Jail), Chance/Community Chest actions, movement to nearest railroad/utility, Jail behavior (3 turns, doubles exit), Go to Jail space.
- **Experiment**: simulate 1,000 games (two players × 150 turns each) and report landing tallies and relative frequencies.

---

## Key behaviors verified (from output)
- **Go to Jail** triggers correctly; turn ends on incarceration.  
- **Doubles**: third consecutive doubles sends player to **Jail**; doubles in Jail free the player.  
- **Card effects**: “Advance to Go,” “Nearest Railroad/Utility,” “Go to Jail,” etc., produce expected board positions.  
- **Long-run results**: **Jail** is the most frequently tallied location; high-traffic spaces include railroads and several orange/red properties (see 1k-game table/plots in the PDF).

---

## Reproduce
1. Open the Rmd in RStudio (R ≥ 4.2).
2. Ensure required class definitions are sourced (as referenced in the top of the Rmd).
3. Knit to HTML/PDF to regenerate the output and plots.

---