# f1-telemetry-analysis

Formula 1 telemetry analysis with Python and [FastF1](https://docs.fastf1.dev/).

> 🚧 **Work in progress.** Analyses, charts and conclusions will be added as the project moves forward.

## Goal

Answer a simple question using official F1 data:

> **Why was one driver faster than another?**

This is also a learning project for data analysis with **pandas**, **numpy** and **matplotlib**.

## Progress

| Step | Notebook | Status |
|---|---|---|
| Setup and FastF1 cache | `01_exploration` | ✅ Done |
| Loading a session | `01_exploration` | ✅ Done |
| Exploring lap data | `01_exploration` | 🚧 In progress |
| Comparing the race pace of two drivers | `02_comparaison_pilotes` | ⏳ Planned |
| Charts (lap times, consistency) | `03_graphiques` | ⏳ Planned |
| Telemetry: where the difference is made | `04_telemetrie` | ⏳ Planned |
| Extracting reusable functions | `src/` | ⏳ Planned |

> The notebooks themselves are written in French.

## Project structure

```
f1-telemetry-analysis/
├── image/        exported charts (for this README)
├── notebooks/    exploration and analyses, one notebook per step
├── src/          reusable functions (planned)
├── requirements.txt
└── README.md
```

## Installation

```bash
python -m venv .venv
source .venv/bin/activate        # bash / zsh (Linux, macOS)
source .venv/bin/activate.fish   # fish
pip install -r requirements.txt
```

### Formula 1 account

Since FastF1 3.9, lap and telemetry data require signing in to a Formula 1 account.
Without it, only session results are available.
Sign in once, from a terminal, with the virtual environment activated:

```bash
python -m fastf1 auth f1tv --authenticate
```

Check the sign-in status:

```bash
python -m fastf1 auth f1tv --status
```

## Running Jupyter

From the root of the repo:

```bash
jupyter lab
```

The notebooks are in `notebooks/` and are meant to be read in order (01, 02, 03, 04).
The FastF1 cache is stored in `cache/` at the root (ignored by Git).

## Results

*Coming soon.*

## License

[MIT](LICENSE)
