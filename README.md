# Movie Revenue Prediction

This repository contains a machine learning project for estimating movie box
office revenue from features such as genre, rating, runtime, budget, release
year, IMDb score, votes, director, writer, cast, country, and production
company.

This version is prepared as a coursework demonstration. It is based on an
existing open-source project and has been adapted for local setup, explanation,
and demo use. Original authorship and license information are retained in the
license and attribution sections below.

## Demo Overview

The project provides:

- A Streamlit web interface for entering movie details and viewing predictions.
- A command line interface for revenue prediction.
- Multiple regression models for comparing prediction quality.
- Feature engineering and preprocessing scripts for model training.
- A revised movie dataset used by the Streamlit app and model scripts.

## My Demo Changes

- Prepared the repository for a classroom demonstration.
- Added a final success/flop status in the Streamlit prediction result by
  comparing predicted revenue with the entered budget.
- Cleaned the README so the main page focuses on setup, usage, and explanation.
- Kept attribution and licensing information separate from the demo flow.

## Project Structure

```text
Movie-Revenue-Prediction/
|-- Helper files/
|-- Misc/
|-- Reports/
|-- fig/
|-- models/
|-- old datasets/
|-- revised datasets/
|-- main.py
|-- streamlit_app.py
|-- requirements.txt
|-- LICENSE
`-- README.md
```

## Setup

Create and activate a Python virtual environment:

```bash
python -m venv env
```

On Windows PowerShell:

```bash
.\env\Scripts\Activate.ps1
```

On macOS/Linux:

```bash
source env/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

## Run The Streamlit App

```bash
streamlit run streamlit_app.py
```

The app asks for movie details, predicts expected revenue, classifies the
predicted revenue range, and shows whether the predicted revenue is above or
below the entered budget.

## Run The CLI

```bash
python main.py
```

Follow the prompts to enter movie attributes and choose a model.

## Model Scripts

Model implementations are available in the `models/` directory:

- `linear_regression.py`
- `decision_tree.py`
- `decision_tree_bagging.py`
- `random_forest.py`
- `gradient_boost.py`
- `XGBoost.py`
- `tracking_XGBoost.py`

The preprocessing flow includes categorical label encoding, numerical
imputation, scaling, log transformation of skewed revenue and budget values,
and engineered ratio/binary features.

## Dataset

The app uses `revised datasets/output.csv`. Dataset notes are available in
`revised datasets/README.md`. The source dataset is the public Movie Industry
dataset from Kaggle.

## Model Evaluation

The project compares models using R2 score and MSLE. The strongest results in
the included evaluation are from Gradient Boosting and XGBoost-style models,
which generally perform better than the simpler baseline regressors.

## Attribution

This repository is adapted from the open-source Movie Revenue Prediction
project by Vikranth Udandarao and Pratyush Gupta. The original research/project
materials include:

- Paper: Movie Revenue Prediction using Machine Learning Models
- arXiv: `2405.11651`
- Dataset source: Movie Industry dataset on Kaggle

This adapted version is for coursework demonstration and keeps the original MIT
license notice in `LICENSE`.

## License

This project is distributed under the MIT License. See `LICENSE` for the
original copyright and license terms.
