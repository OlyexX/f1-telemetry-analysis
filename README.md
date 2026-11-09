# f1-telemetry-analysis

Analyse de télémétrie de Formule 1 avec Python et [FastF1](https://docs.fastf1.dev/).

> 🚧 **Projet en cours de réalisation.** Les analyses, les graphiques et les conclusions arrivent au fil de l'avancement.

## Objectif

Répondre à une question simple à partir des données officielles de la F1 :

> **Pourquoi tel pilote a-t-il été plus rapide que tel autre ?**

C'est aussi un projet d'apprentissage de l'analyse de données avec **pandas**, **numpy** et **matplotlib**.

## Avancement

| Étape | Notebook | État |
|---|---|---|
| Mise en place et cache FastF1 | `01_exploration` | ✅ Terminé |
| Chargement d'une session | `01_exploration` | ✅ Terminé |
| Exploration des données de tours | `01_exploration` | 🚧 En cours |
| Comparaison du rythme de deux pilotes | `02_comparaison_pilotes` | ⏳ À venir |
| Graphiques (temps au tour, régularité) | `03_graphiques` | ⏳ À venir |
| Télémétrie : où se fait la différence | `04_telemetrie` | ⏳ À venir |
| Extraction des fonctions réutilisables | `src/` | ⏳ À venir |

## Structure du projet

```
f1-telemetry-analysis/
├── image/        graphiques exportés (pour ce README)
├── notebooks/    exploration et analyses, un notebook par étape
├── src/          fonctions réutilisables (à venir)
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

### Compte Formula 1

Depuis FastF1 3.9, les données de tours et la télémétrie nécessitent une connexion à un compte Formula 1.
Sans connexion, seuls les résultats des sessions sont disponibles.
La connexion se fait une seule fois, dans un terminal, avec l'environnement virtuel activé :

```bash
python -m fastf1 auth f1tv --authenticate
```

Vérifier la connexion :

```bash
python -m fastf1 auth f1tv --status
```

## Lancer Jupyter

Depuis la racine du repo :

```bash
jupyter lab
```

Les notebooks sont dans `notebooks/` et se lisent dans l'ordre (01, 02, 03, 04).
Le cache FastF1 est stocké dans `cache/` à la racine (ignoré par Git).

## Résultats

*À venir.*

## Licence

[MIT](LICENSE)
