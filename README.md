# AF Prediction using the East London Database

Machine learning project to predict 5-year incident atrial fibrillation (AF) risk in adults using primary care electronic health records from the East London Database (ELD).

## Project status
In development — learning project using ELD-structured synthetic data.

## Goal
Build a binary classifier that predicts whether a patient without AF at baseline will develop AF within 5 years, using demographic and clinical features available in ELD-style GP records.

## Repository structure

- data/raw/ — source data (gitignored)
- data/processed/ — cleaned/feature-engineered data (gitignored)
- data/synthetic/ — toy dataset for development
- notebooks/ — exploratory analysis
- src/ — reusable pipeline code (cohort, features, models, evaluate)
- models/ — saved model artefacts (gitignored)
- reports/ — figures, tables, writeups
- tests/ — unit tests

## Pipeline overview
1. Cohort extraction: adults 40+, registered 1yr+, no prior AF
2. Feature engineering: demographics, QOF registers, process measures
3. Temporal train/validation/test split
4. Baselines (trivial, CHARGE-AF, logistic regression) then main models
5. Evaluation: discrimination, calibration, subgroup fairness

## Setup

    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt

## Data
This project does NOT use real patient data. All development uses synthetic data shaped like ELD variables. Real ELD access is governed by the Clinical Effectiveness Group at Queen Mary University of London and requires accreditation.

## License
MIT
