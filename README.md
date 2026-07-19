# CodeAlpha_IrisClassification
"ML based Iris flower Classification comparing 6 algorithms with cross-validation | CodeAlpha Internship"
# CodeAlpha_IrisClassification

## 📌 Overview
This project is part of the **CodeAlpha Data Science Internship**. It classifies Iris flowers into three species — **Setosa, Versicolor, and Virginica** — based on their sepal and petal measurements, using multiple machine learning algorithms.

## 📊 Dataset
- **Source:** Built-in Iris dataset from `scikit-learn` (`sklearn.datasets.load_iris`)
- **Samples:** 150 (50 per species)
- **Features:** Sepal length, Sepal width, Petal length, Petal width (all in cm)
- **Target:** Species (Setosa / Versicolor / Virginica)

## 🔧 What This Project Does
1. **Data Exploration (EDA)** — summary statistics, class balance, correlation, skewness, per-species comparisons
2. **Visualization** — pairplots, correlation heatmap, boxplots, violin plots, histograms, scatter plots
3. **Preprocessing** — train-test split, feature scaling (StandardScaler)
4. **Model Training** — 6 classification algorithms:
   - Logistic Regression
   - K-Nearest Neighbors (KNN)
   - Decision Tree
   - Support Vector Machine (SVM)
   - Random Forest
   - Naive Bayes
5. **Model Evaluation** — 10-fold cross-validation (not just a single train/test split) for a reliable performance comparison
6. **Feature Importance** — identifies which measurements matter most for classification
7. **Prediction** — demonstrates predicting the species of a new flower sample

## 🏆 Results

| Model | Mean CV Accuracy | Std Dev |
|---|---|---|
| **K-Nearest Neighbors** | **96.00%** | 0.053 |
| Logistic Regression | 95.33% | 0.052 |
| Naive Bayes | 95.33% | 0.052 |
| Support Vector Machine | 94.67% | 0.058 |
| Random Forest | 94.67% | 0.058 |
| Decision Tree | 93.33% | 0.052 |

**Best model: K-Nearest Neighbors**, based on 10-fold cross-validation across the full dataset.

Cross-validation was used instead of a single train-test split because, with only 150 samples, a single split leaves just 30 test rows — a couple of misclassifications can swing accuracy significantly. 10-fold CV evaluates each model across the entire dataset for a much more reliable comparison.

### Key Insight
Petal length and petal width are by far the most important features for classification (~87% combined importance), while sepal width contributes the least. Setosa is linearly separable from the other two species on every feature, while Versicolor and Virginica show some overlap.

## 🛠️ Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

## ▶️ How to Run
1. Clone this repository
2. Install dependencies:
   ```
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
3. Run the script:
   ```
   python iris_classification.py
   ```
   or open it in Jupyter Notebook and run all cells.

## 📁 Files
- `iris_classification.py` — full project code (EDA, visualization, model training, evaluation)

## 🎓 Internship
This project was completed as part of the **CodeAlpha Data Science Internship**.
