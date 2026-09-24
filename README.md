# Comparaison de MLP et régularisations

Projet extrait du notebook `optimisation-d-une-mlp-dans-sa-regularisation.ipynb`.

Il compare trois perceptrons multicouches (MLP) sur le jeu de données **Breast Cancer Wisconsin** de scikit-learn :

- Un MLP baseline sans régularisation.
- Un MLP avec régularisation L2.
- Un MLP avec régularisation personnalisée des activations : pénalité de sparsité par divergence KL et pénalité anti-saturation fondée sur l'écart-type.

> Le notebook fourni ne traite pas la détection d'URLs malveillantes : l'arborescence a donc été adaptée au véritable sujet du code.

## Installation

```bash
python -m venv .venv
source .venv/bin/activate  # Windows : .venv\Scripts\activate
pip install -r requirements.txt
```

## Exécution

Depuis la racine du projet :

```bash
python src/train.py
```

Pour un essai rapide :

```bash
python src/train.py --epochs 10
```

## Sorties générées

- `models/mlp_baseline.keras`
- `models/mlp_l2.keras`
- `models/mlp_distribution.keras`
- `results/figures/confusion_matrix_<modele>.png`
- `results/figures/history_<modele>.png`
- `results/metrics/<modele>_metrics.json`
- `results/metrics/comparison.csv`

## Organisation

```text
src/config.py       # Paramètres et chemins
src/data_loader.py  # Chargement, division et standardisation
src/model.py        # MLP et couche ActivationRegularization
src/train.py        # Entraînement, évaluation et sauvegarde
src/evaluate.py     # Métriques et visualisations
src/utils.py        # Reproductibilité et utilitaires
```
