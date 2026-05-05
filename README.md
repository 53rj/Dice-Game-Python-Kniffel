# Dice Game — Kniffel (Yahtzee)

A **terminal-based dice game** (German rules: *Kniffel*, equivalent to *Yahtzee*) written in Python. This repository contains a small first-semester IT project: local multiplayer on the command line, score tracking on a printable-style score sheet, and classic reroll mechanics.

## Features

- **2 rerolls per turn** — keep any dice (`ja` / `nein`), then reroll selected dice by typing `w1`–`w5`
- **13 scoring categories** — upper section (1s–6s) with **63-point bonus** (+35), lower section (three-of-a-kind through chance)
- **Multiple players** — one shared score table; winner determined by total score after full rounds
- **Intro sequence** — loading animation and ASCII logo on startup

## Requirements

- **Python 3.x** (standard library only; no pip packages required)

## How to run

From the repository root:

```bash
cd Kniffel
python main.py
```

On some systems use `python3` instead of `python`.

All prompts and in-game text are in **German** (`ja` / `nein`, category names, etc.).

## Project layout

| File | Role |
|------|------|
| `Kniffel/main.py` | Entry point: setup loop and game flow |
| `Kniffel/menu.py` | Splash screen, player count, names, start confirmation |
| `Kniffel/game.py` | Turns, dice rolling & rerolls, score entry, totals, winner |
| `Kniffel/daten.py` | Score sheet layout and final table output |
| `Kniffel/liste.py` | Scoring rules (upper/lower combinations) |

## Game flow (short)

1. Enter number of players and each player’s name.
2. Confirm start with `ja` or cancel with `nein`.
3. Each turn: roll five dice, optionally reroll up to twice, then choose category **1–13** to record the result (each cell once per player).
4. After **13 rounds per player**, the final standings and winner are shown.

## Authors

**Sergiy Stuempel** & **Markus Finger** — IT project, 1st semester.

## License

No license file is included in this repository. Add a `LICENSE` file if you want to clarify terms of use.
