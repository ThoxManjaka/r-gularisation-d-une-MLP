# Comparaison de MLP et régularisations

Il compare trois perceptrons multicouches (MLP) sur le jeu de données **Breast Cancer Wisconsin** de scikit-learn :

- Un MLP baseline sans régularisation.
- Un MLP avec régularisation L2.
- Un MLP avec régularisation personnalisée des activations : pénalité de sparsité par divergence KL et pénalité anti-saturation fondée sur l'écart-type.

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
