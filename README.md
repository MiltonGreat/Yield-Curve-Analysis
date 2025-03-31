# Yield Curve Analysis for Recession Prediction

![screenshot-localhost_8888-2025 03 31-09_04_26](https://github.com/user-attachments/assets/6ad0611e-b2fe-4ef6-b22a-82e595aee179)

## Overview
This project explores the relationship between yield curve inversions and economic recessions. By analyzing bond yield spreads (specifically the 10-year and 2-year yields) from US bond market data spanning 1990-2019, the goal is to predict recessions based on these yield curve movements. The project utilizes machine learning models, specifically K-Nearest Neighbors (KNN), to predict the probability of a recession and assesses the model's performance using various evaluation metrics.

### Objectives

1. Analyze bond yield spreads to identify yield curve inversions, specifically the 10Y-2Y spread, and its potential to signal upcoming recessions.

2. Predict recessions using K-Nearest Neighbors (KNN) model.

3. Evaluate model performance with metrics such as accuracy, precision, recall, and F1-score.

4. Handle class imbalance in the dataset to improve model performance.

### Dataset

The dataset consists of US bond yield data from 1990 to 2019, which includes:

- 3-month yield
- 2-year yield
- 10-year yield

The data is used to calculate various yield curve spreads, which are key indicators of potential economic downturns.

### Steps in the Project

1. Data Preprocessing

Calculate Yield Curve Spreads:
- 10Y-2Y spread (difference between 10-year and 2-year yields).
- 10Y-3M spread (difference between 10-year and 3-month yields).
- Synthetic 5Y spread (average of 10-year and 3-month yields minus 2-year yield).

2. Visualize Yield Curve

The yield curve levels (3-month, 2-year, 10-year) and yield spreads (10Y-2Y, 10Y-3M) are visualized using plots to better understand the trends and identify inversions (when the spreads turn negative).

3. Recession Prediction

Recession Indicator:
- A yield curve inversion (10Y-2Y < 0) is considered a signal of a potential recession.
- A 12-month lead is applied to predict recessions in advance.

Model Training:
- The K-Nearest Neighbors (KNN) model is trained on the data, and performance metrics are calculated.
- The model is evaluated based on its ability to predict recessions using the yield curve spreads.

4. Model Evaluation

Accuracy Metrics:

The performance of the KNN model is evaluated using the following metrics:
- Precision: Proportion of true positives (recessions predicted correctly).
- Recall: Proportion of actual recessions correctly predicted.
- F1-Score: Harmonic mean of precision and recall.
- Accuracy: Overall correct predictions.

5. Handling Class Imbalance

The class distribution is imbalanced, with fewer recessions (1.0) than non-recessions (0.0). Resampling techniques are applied to balance the classes and improve the model's ability to predict recessions.

6. Model Performance After Adjustments

The KNN model's performance is assessed after applying resampling techniques and adjustments to the class imbalance, focusing on improvements in precision and recall.

### Results

The yield curve analysis indicated that yield curve inversions, particularly when the 10Y-2Y spread turned negative, were strong indicators of upcoming recessions. The KNN model was able to predict recessions but struggled with imbalanced classes. After handling class imbalance through resampling, the model's performance improved but still showed limitations in predicting the minority class (recessions).

### Challenges

- Class Imbalance: The dataset contained more non-recession periods than recession periods, leading to biased predictions favoring the majority class.

- Model Limitations: The KNN model, while useful, struggled with predicting recessions due to the historical nature of bond yield data and the noisy nature of economic events.

### Future Work

- Model Improvements: Exploring alternative models such as Random Forest, XGBoost, or neural networks to improve prediction accuracy.

- Feature Engineering: Investigating other potential features or combinations of yield spreads to improve model performance.

- Class Weighting: Applying class weighting in the KNN model to better handle class imbalance.

### Conclusion

This project provides valuable insights into the potential of using bond yield spreads to predict economic recessions. Although the KNN model demonstrated some promise, there are several opportunities to enhance the analysis through improved models, better handling of class imbalance, and feature engineering.

### Source

![U.S. Treasury Yields from Kaggle](https://www.kaggle.com/datasets/guillemservera/us-treasury-yields-daily)

