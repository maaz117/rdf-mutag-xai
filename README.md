# MUTAG Mutagenicity Prediction

## Task
Predict whether a chemical compound is mutagenic
using the MUTAG RDF dataset and explain predictions with SHAP.

## Dataset
MUTAG dataset from:
https://data.dgl.ai/dataset/rdf/mutag-hetero.zip

Place the following files in data/ folder:
- mutag_stripped.nt
- completeDataset.tsv
- trainingSet.tsv
- testSet.tsv

## Setup
conda create -n xai26-mini python=3.12
conda activate xai26-mini
pip install -r requirements.txt

## Run
Open and run mutag.ipynb top to bottom.
All cells must be run in order.

## Results
- Best model: GradientBoosting (75.0% test accuracy)
- SHAP explanations identify structural features
  (five_ring, amine, alkyl_halide) as key predictors

## Code Quality
nbqa flake8 mutag.ipynb --max-line-length=120 --ignore=W503,E501

## Team
- Maaz Adnan - (4110700)
- Muhammad Ali - (4107433)
