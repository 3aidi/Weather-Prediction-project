# Weather Prediction Using Machine Learning

## Project Description

This project predicts daily weather conditions (sun, rain, fog, drizzle, snow) using machine learning classification algorithms. The models are trained on the **Seattle Weather Dataset** (2012–2015) which contains 1,461 daily weather records.

Four algorithms are implemented and compared:
- Random Forest
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- XGBoost

Each model is evaluated using Accuracy, Precision, Recall, F1-score, and Confusion Matrix.

## Team Members

| Name               | Student ID |
|--------------------|------------|
| Keroles Amgad      | 224101546  |
| Mahmoud Elaidi     | 224101559  |
| Mahmoud Mohamed    | 224101560  |
| Youssef Mahmoud    | 224101567  |

## Dataset

- **Name:** Seattle Weather Dataset
- **Source:** [Kaggle — Weather Prediction](https://www.kaggle.com/datasets/ananthr1/weather-prediction)
- **Loaded from:** `https://vega.github.io/vega-datasets/data/seattle-weather.csv` (no local file needed)
- **Records:** 1,461 rows — 80% train / 20% test (stratified split, `random_state=42`)
- **Features:** `precipitation`, `temp_max`, `temp_min`, `wind`
- **Target:** `weather` — 5 classes: drizzle, fog, rain, snow, sun

## Project Structure

```
├── Weather_Prediction.ipynb   # Main notebook with all code, models, and results
└── README.md                  # This file
```

> The dataset is fetched automatically from the web — no local CSV file is required.

## How to Run

1. Install the required libraries:
   ```
   pip install numpy pandas matplotlib seaborn scikit-learn xgboost
   ```
   > Requires **XGBoost 2.0+** (default with the command above).
2. Open `Weather_Prediction.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
3. Click **Run All** — the dataset is downloaded automatically.

## Model Configuration

| Model         | Key Hyperparameters                                          |
|---------------|--------------------------------------------------------------|
| Random Forest | `n_estimators=200`, `random_state=42`                        |
| KNN           | `n_neighbors=7` (trained on scaled features)                 |
| SVM           | `kernel='rbf'`, `C=1.0` (trained on scaled features)        |
| XGBoost       | `n_estimators=200`, `max_depth=4`, `learning_rate=0.1`      |

> KNN and SVM use `StandardScaler`-normalized features; Random Forest and XGBoost use raw features.

## Results Summary

| Model         | Accuracy | Precision | Recall | F1-Score |
|---------------|----------|-----------|--------|----------|
| Random Forest | 0.6587   | 0.6376    | 0.6587 | 0.6428   |
| KNN           | 0.6382   | 0.6083    | 0.6382 | 0.6161   |
| SVM           | 0.6553   | 0.6134    | 0.6553 | 0.6101   |
| XGBoost       | 0.6280   | 0.6122    | 0.6280 | 0.6180   |

**Best Model:** Random Forest (highest F1-score: 0.6428)

## Tools and Libraries

- Python 3
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
