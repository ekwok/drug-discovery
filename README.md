# Computational Drug Discovery
Machine learning for predicting activity of inhibitory compounds against the influenza A virus

## Part 1 - Download Bioactivity Data
From the [ChEMBL Database](https://www.ebi.ac.uk/chembl/), download bioactivity data of compounds that act as inhibitors against influenza A.

Output files:
- `influenza_a_bioactivity.csv`
- `influenza_a_preprocessed.csv`

## Part 2 - Exploratory Data Analysis
Calculate Lipinski descriptors for drug-likeness and perform exploratory data analysis on those new features. Conduct Mann-Whitney U Test to determine whether or not the distributions of active and inactive compounds differ by a significant amount.

Input file:
- `influenza_a_preprocessed.csv`

Output file:
- `influenza_a_pIC50.csv`

## Part 3 - Descriptor Calculation
Calculate molecular fingerprint descriptors from the `canonical_smiles` feature of each compound.

Input file:
- `influenza_a_pIC50.csv`

Output file:
- `influenza_a_pIC50_pubchem_fp.csv`

## Part 4 - Build Machine Learning Model
Using a random forest regressor, build a machine learning model to predict the activity of inhibitors against the influenza A virus.

Input file:
- `influenza_a_pIC50_pubchem_fp.csv`

Output file:
- `predictions.csv`
