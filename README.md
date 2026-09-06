# Diabetes Prediction (Azure)

A Flask app that predicts whether a patient is diabetic from the standard Pima Indians Diabetes dataset features, packaged for deployment on Azure.

> Closely related to [Diebetese_prediction_model](https://github.com/yaseensiddiqui36/Diebetese_prediction_model) — same dataset and approach, this version is wired for Azure App Service paths.

## Tech Stack

Python, Flask, scikit-learn, pandas, seaborn (EDA).

## Features

- EDA + model training notebook (`Notebooks/Diabetes_Prediction_Azure.ipynb`).
- Trained classifier + `StandardScaler`, pickled (`Models/Diabetese_prediction_azure_model.pkl`, `Models/standardScalar.pkl`).
- Flask app (`application.py`) with a home form (`/predictdata`) taking Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigreeFunction, and Age, returning a Diabetic/Non-Diabetic result.

## Setup & Usage

```bash
pip install -r requirements.txt
python application.py
```

Note: `application.py` loads pickles from a hardcoded `/config/workspace/Models/...` path (left over from its original Azure ML notebook environment) — update those paths to run locally.

## Status

Working prediction model with a Flask front end. Not actively maintained.
