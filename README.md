# Extreme Risk AI

Analyse des risques climatiques extrêmes à partir des données NOAA Storm Events.

> 🚧 **Projet en cours** — seule une première exploration des données a été réalisée. Aucune analyse des pertes ni aucun modèle n'a encore été développé.

## Objectif

À terme, étudier les pertes liées aux événements extrêmes, rares mais potentiellement très coûteux, en commençant par les inondations. Le projet est un travail d'apprentissage personnel ; les étapes et résultats seront documentés au fur et à mesure.

## Démarche

Le cadrage du problème est détaillé dans [docs/comprendre_le_probleme.md](docs/comprendre_le_probleme.md).

## Données

Source : [NOAA Storm Events Database](https://www.ncei.noaa.gov/stormevents/), fichier « details » pour l'année 2024.

Télécharger le fichier détaillé 2024 depuis la NOAA et le placer dans `data/raw/` (sous-dossier de `data/`, déjà utilisé par le notebook). Les fichiers de données ne sont pas suivis par Git.

## Avancement

- [x] Environnement virtuel et dépendances
- [x] Chargement et première exploration (51 variables, types d'événements)
- [x] Filtrage des inondations : 2 472 `Flood`, 4 661 `Flash Flood`
- [ ] Conversion des montants de dommages (suffixes K, M) et distinction manquant / zéro
- [ ] Statistiques descriptives et visualisations
- [ ] Étude de la queue de distribution des pertes

## Installation

Depuis la racine du dépôt, créer l'environnement virtuel :

```bash
python -m venv .venv
```

L'activer, puis installer les dépendances et lancer Jupyter :

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS / Linux
source .venv/bin/activate

pip install -r requirements.txt
jupyter notebook
```

Le notebook d'exploration se trouve dans `notebooks/01_exploration.ipynb`.

## Technologies

Python, pandas, NumPy, Matplotlib, SciPy et Jupyter.
