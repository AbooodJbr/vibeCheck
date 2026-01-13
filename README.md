# Personality Prediction

Notebook-driven experiment for predicting introvert vs. extrovert labels from simple behavioral signals. This is a simple project meant to try out a binary personality classifier end-to-end.

## Data
- Source CSV: `data/personality_datasert.csv`
- Columns: time spent alone, stage fear, social activity measures, posting frequency, and a binary `Personality` target.
- Categorical fields are label-encoded (`Yes/No` → 1/0, `Extrovert/Introvert` → 1/0).

## Environment
- Python 3.10+
- Suggested packages: `tensorflow`, `torch`, `pandas`, `numpy`, `scikit-learn`

Install dependencies:
```bash
pip install tensorflow torch pandas numpy scikit-learn
```

## Usage
1) Open `main.ipynb` in VS Code or Jupyter.
2) Run cells in order: version checks → data load/encoding → train/validation split → min–max scaling → TensorFlow model build/fit → quick prediction → metric reports → PyTorch demo.
3) Adjust hyperparameters (layer sizes, batch size, epochs, learning rate) in the model-definition and training cells as needed.
4) Review printed metrics: accuracy plus confusion matrix, precision, recall, F1, and ROC AUC.

## Notes
- Min–max scaling is applied only to feature columns; the target label remains binary.
- Over/underfitting heuristics print after training, along with extended validation metrics.
- The PyTorch section mirrors the TensorFlow pipeline for comparison.
