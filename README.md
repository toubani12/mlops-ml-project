# mlops-ml-project — baseline ML reproductible

Baseline de classification sur le dataset Iris (intégré à scikit-learn) :
configuration YAML, modules réutilisables dans `src/`, scripts dans `scripts/`.

## Installation
python -m venv .venv
.venv\Scripts\Activate.ps1               # Linux/macOS : source .venv/bin/activate
pip install -r requirements.txt

(Avec uv : `uv sync` installe les versions exactes de `uv.lock`.)

## Entraînement
python scripts/train.py

## Évaluation
python scripts/evaluate.py

## Tests
python -m pytest -q

## Artefacts (générés dans artifacts/, non versionnés)
- model.joblib : pipeline entraîné (prétraitement + modèle)
- metrics.json : accuracy et f1_macro sur le jeu de test
- confusion_matrix.png : matrice de confusion
- report.json : rapport de classification détaillé
