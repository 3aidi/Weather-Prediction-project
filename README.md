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
| Mohamed Elsayed    | 224101551  |
| Mahmoud Saad       | 224101559  |
| Mahmoud Mohamed    | 224101560  |
| Youssef Mahmoud    | 224101567  |

## Dataset

- **Name:** Seattle Weather Dataset
- **Source:** [Kaggle — Weather Prediction](https://www.kaggle.com/datasets/ananthr1/weather-prediction)
- **File:** `seattle-weather.csv`
- **Records:** 1,461 rows
- **Features:** precipitation, temp_max, temp_min, wind
- **Target:** weather (drizzle, fog, rain, snow, sun)

## Project Structure

```
├── Weather_Prediction.ipynb   # Main notebook with all code, models, and results
├── seattle-weather.csv        # Dataset
└── README.md                  # This file
```

## How to Run

1. Install the required libraries:
   ```
   pip install numpy pandas matplotlib seaborn scikit-learn xgboost
   ```
2. Place `seattle-weather.csv` in the same folder as the notebook.
3. Open `Weather_Prediction.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab.
4. Click **Run All**.

## Results Summary

| Model         | Accuracy | Precision | Recall | F1-Score |
|---------------|----------|-----------|--------|----------|
| Random Forest | 0.6587   | 0.6376    | 0.6587 | 0.6428   |
| KNN           | 0.6382   | 0.6083    | 0.6382 | 0.6161   |
| SVM           | 0.6553   | 0.6134    | 0.6553 | 0.6101   |
| XGBoost       | 0.6280   | 0.6122    | 0.6280 | 0.6180   |

**Best Model:** Random Forest (highest F1-score)

## Tools and Libraries

- Python 3
- NumPy, Pandas
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
