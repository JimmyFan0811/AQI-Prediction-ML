# AQI Prediction Using Machine Learning

This repository contains an undergraduate project on **Air Quality Index (AQI) prediction using machine learning**, developed with **RapidMiner Studio**.

The project investigates the use of meteorological and air-pollution data for AQI classification, with particular attention to **class imbalance**, model evaluation, and sampling strategies.

## Project Overview

Air Quality Index (AQI) provides a standardized measure of air pollution severity.

This project explores a machine-learning workflow for AQI prediction using environmental variables such as:

- Air pollutant measurements
- Meteorological variables
- Historical AQI-related information

The project covers the complete workflow from data preparation to model evaluation.

## Machine Learning Workflow

The RapidMiner workflow includes:

1. Data loading and preprocessing
2. Attribute selection
3. AQI transformation into a binary classification target
4. Training / testing data split
5. Support Vector Machine (SVM) training
6. Prediction on the test set
7. Performance evaluation

The primary implementation uses a **Support Vector Machine (SVM)** classifier.

## Handling Imbalanced Data

Because AQI classes may be imbalanced, an additional workflow was developed using
**SMOTE (Synthetic Minority Over-sampling Technique)**.

The SMOTE workflow includes:

- Minority-class oversampling
- SVM model training
- Prediction on held-out data
- Accuracy evaluation
- ROC-AUC evaluation
- Precision-Recall / AUPRC evaluation

This allows the model to be evaluated using metrics that are more informative than accuracy alone for imbalanced classification problems.

## Evaluation Metrics

The project considers several classification metrics:

- **Accuracy**
- **Confusion Matrix**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC**
- **AUPRC**

In the project report, one SMOTE-based experiment achieved:

| Metric | Result |
|---|---:|
| Accuracy | 76.23% |
| ROC-AUC | 0.810 |
| AUPRC | 0.843 |

## Dataset

The dataset contains air-quality and meteorological variables, including measurements such as:

- AQI
- SO2
- CO
- PM10
- PM2.5
- NO2
- O3
- Temperature
- Humidity
- Wind information
- Rainfall
- UV-related information

The data were used to investigate relationships between environmental conditions and AQI levels.

## Repository Structure

- `workflows/`
  - `aqi_svm_classification.rmp` — main SVM classification workflow
  - `aqi_smote_sampling.rmp` — SVM workflow with SMOTE for imbalanced data

- `data/`
  - `aqi_dataset.csv` — project dataset

- `docs/`
  - `aqi_prediction_report.pdf` — project presentation and technical report

- `figures/`
  - selected model evaluation and workflow figures

## Technical Topics

- Machine Learning
- Support Vector Machine
- Data Preprocessing
- Binary Classification
- Imbalanced Data
- SMOTE
- Confusion Matrix
- ROC-AUC
- Precision-Recall Curve
- AUPRC
- Air Quality Prediction

## Tools

- **RapidMiner Studio**
- CSV data processing
- Machine Learning
- Statistical model evaluation

## Publication

The results of this undergraduate project were subsequently published in:

*Journal of Big Data Application and Management*,  
Vol. 4, 2024, pp. 1–5.
