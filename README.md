# Student Performance Prediction using XGBoost

This project focuses on building a robust Machine Learning pipeline to predict student performance (Classification) using **XGBClassifier**, Performed Hyperparameter Tuning using **GridSearchCV** to optimize depth and learning rates, The model evaluates various academic and behavioral features to make accurate predictions.

## 🚀 Project Overview & Strategy
During the development phase, a key focus was placed on model reliability rather than just chasing high metrics. 
* **Handling Data Leakage:** The initial model achieved a perfect F1-Score of `1.0000`. Through rigorous feature importance analysis, a major **Data Leakage** issue was identified in the final column. Removing this leaking feature brought the model down to a realistic, highly robust, and deployable performance.
* **Manual Logic vs. Automated Libraries:** Built with a deep understanding of evaluation metrics from scratch to ensure true model generalization.

## 📊 Evaluation Metrics
* **Final F1-Score:** `0.8905` (A well-balanced score between Precision and Recall, proving the model handles class distributions effectively without cheating).

## 🔍 Feature Importance Analysis
We evaluated the features using two different approaches from XGBoost to understand the model's inner decision-making process:

1. **Weight (Frequency):** Counts how many times a feature is used to split the data across all trees.
2. **Gain (Contribution):** Measures the actual quality and accuracy improvement brought by a feature. 

*Result:* **`study_hours_per_week`** emerged as the most dominant feature in both metrics, followed by **`previous_score`** and **`attendance_rate`**. Lower-impact features like `internet_access` and `extracurricular` are candidates for future pruning.

## 🛠️ Tech Stack
* Python
* XGBoost
* Scikit-Learn
* Pandas & NumPy

## 🔮 Future Work
* Deploy the model as a production-ready web service using **FastAPI**.
