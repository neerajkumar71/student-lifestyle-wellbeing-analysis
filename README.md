# Student Lifestyle and Wellbeing Analysis

### An Exploratory Data Analysis, Statistical Testing, Machine Learning, and NLP Project

## 📌 Project Overview

The **Student Lifestyle and Wellbeing Analysis** project explores the relationship between students' daily habits and their mental health scores. It uses Python, data visualization, statistical hypothesis testing, machine learning, and Natural Language Processing (NLP) to identify patterns in student lifestyle data.

The project examines factors such as daily usage hours, phone unlocks, study time, physical activity, and sleep duration to understand how they are associated with wellbeing scores.

## 🎯 Project Objectives

- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA) using graphs and visualizations.
- Study relationships between lifestyle habits and mental health scores.
- Perform statistical hypothesis testing using Pearson correlation.
- Develop and evaluate regression and classification models.
- Analyze lifestyle reflection text using NLP techniques.
- Compare machine learning models and identify the best-performing models.

## 🗂️ Dataset Description

The project uses an augmented student lifestyle and wellbeing dataset containing **5,015 rows and 15 columns** before preprocessing.

Important features include:

- `Age`
- `Gender`
- `Country`
- `Academic_Level`
- `Most_Used_Platform`
- `Purpose_Of_Use`
- `Avg_Daily_Usage_Hours`
- `Daily_Unlocks`
- `Study_Hours`
- `Physical_Activity_Hours`
- `Sleep_Hours_Per_Night`
- `Stress_Level`
- `Mental_Health_Score`
- `Synthetic_Lifestyle_Reflection`

The dataset is cleaned by handling missing values, removing duplicate records, standardizing categorical values, and checking invalid numerical values.

**Note:** The dataset is augmented, and the lifestyle reflections are synthetic. Therefore, the findings should be interpreted cautiously and should not be generalized to all students without validation.

## 🛠️ Technologies and Libraries

- **Python** — Programming language
- **Jupyter Notebook** — Implementation environment
- **Pandas** — Data manipulation and cleaning
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Scikit-learn** — Machine learning and model evaluation
- **NLTK** — Text preprocessing
- **WordCloud** — Text visualization
- **SciPy** — Statistical testing

## 📊 Exploratory Data Analysis (EDA)

EDA is performed to understand the dataset and identify patterns in student lifestyle and wellbeing.

The notebook includes:

1. Distribution of mental health scores.
2. Relationship between sleep hours and mental health scores.
3. Correlation heatmap of numerical features.

These visualizations help explore the distribution of scores and the relationships between lifestyle variables.

## 📈 Statistical Analysis

Pearson correlation is used to examine the relationship between `Sleep_Hours_Per_Night` and `Mental_Health_Score`.

- **Null Hypothesis (H₀):** There is no linear correlation between sleep hours and mental health scores in the population.
- **Alternative Hypothesis (H₁):** There is a linear correlation between sleep hours and mental health scores in the population.
- **Significance Level:** 0.05

The notebook reports a positive Pearson correlation of approximately **0.408**, with a p-value below 0.05. Therefore, the null hypothesis is rejected for this analysis.

This indicates a statistically significant positive association in the analyzed dataset. Correlation does not establish causation.

## 🤖 Machine Learning Models

### 1. Regression Models

Regression models predict the numerical `Mental_Health_Score`.

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 0.596 | 0.744 | 0.681 |
| Random Forest Regression | 0.437 | 0.570 | 0.813 |

**Best-performing regression model:** Random Forest Regression, with an R² score of approximately 0.813.

### 2. Classification Models

Classification converts mental health scores into Lower, Middle, and Higher categories using quantile-based binning.

| Model | Accuracy |
|---|---:|
| Logistic Regression | 75.9% |
| Decision Tree | 75.7% |
| Random Forest | 81.4% |
| Support Vector Machine (SVM) | 78.7% |
| K-Nearest Neighbors (KNN) | 77.3% |

**Best-performing classification model:** Random Forest, with an accuracy of approximately 81.4%.

These values represent the current notebook's evaluation results and may vary with different data splits or preprocessing methods.

## 💬 Natural Language Processing (NLP)

NLP techniques are applied to the `Synthetic_Lifestyle_Reflection` column.

The text analysis includes:

- Text cleaning and normalization.
- Stopword removal.
- Word frequency analysis.
- Bar chart visualization of frequent terms.
- Word cloud generation.

This analysis explores common words and themes in the generated lifestyle reflections. Since the text is synthetic, it should not be treated as direct evidence of real students' emotions or mental health.

## 📁 Project Structure

```text
Student-Lifestyle-Wellbeing-Analysis/
│
├── Codes.ipynb
├── moodlens_augmented_unclean.csv
├── Student_Lifestyle_and_Wellbeing_Analysis_Report.docx
└── README.md
```

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install Python and Jupyter Notebook.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn scipy nltk wordcloud
   ```

4. Open `Codes.ipynb` in Jupyter Notebook.
5. Keep the CSV file in the same directory as the notebook, or update the dataset path in the code.
6. Run the notebook cells in order to reproduce the analysis and model evaluation.

## 🔍 Key Findings

- The evaluated dataset shows associations between lifestyle habits and mental health scores.
- Sleep duration has a positive correlation with mental health scores in the Pearson correlation test.
- Random Forest Regression performs better than Linear Regression in the reported regression evaluation.
- Random Forest achieves the highest reported accuracy among the five classification models.
- NLP frequency analysis identifies common terms in the synthetic lifestyle reflections.

These findings are exploratory and do not establish that any lifestyle factor causes a particular mental health outcome.

## ⚠️ Limitations

- The dataset is augmented and may not fully represent real student populations.
- Synthetic text reflections may not capture genuine student experiences.
- Model performance depends on preprocessing, data splitting, and the selected evaluation metrics.
- Statistical association does not imply causation.
- The mental health score is a dataset variable and should not be interpreted as a clinical diagnosis.
- Further validation on suitable real-world data is needed before drawing broader conclusions.

## 🔮 Future Scope

- Evaluate models using cross-validation and additional classification metrics.
- Improve preprocessing by fitting imputation steps only on training data.
- Compare additional machine learning algorithms.
- Validate findings using suitable real-world datasets with appropriate privacy safeguards.
- Explore more advanced NLP techniques for text analysis.

## 📝 Conclusion

This project combines data preprocessing, EDA, statistical hypothesis testing, regression, classification, and NLP to study student lifestyle and wellbeing data. Random Forest provides the strongest reported performance in both the regression and classification experiments. The project demonstrates how data analytics and machine learning can help explore patterns in lifestyle datasets while highlighting the importance of careful interpretation, data quality, and validation.

---

**Project:** Student Lifestyle and Wellbeing Analysis  
**Domain:** Predictive Analytics and Data Science  
**Tools:** Python, Jupyter Notebook, Pandas, Seaborn, Scikit-learn, NLTK
