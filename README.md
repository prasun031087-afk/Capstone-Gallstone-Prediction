# Gallstone Disease Prediction using Machine Learning

## Project Overview

This project focuses on predicting the likelihood of **gallstone disease (cholelithiasis)** using machine learning techniques. The study leverages a structured dataset (from the UCI repository) and applies multiple classification algorithms to identify key risk factors and build predictive models.

The objective is to support early diagnosis and improve clinical decision-making using data-driven insights.

## Dataset

* Source: UCI Machine Learning Repository
* Domain: Healthcare / Clinical Data
* Target Variable: Presence or absence of gallstone disease
* Features include:

  * Demographic attributes (age, gender, etc.)
  * Clinical measurements
  * Lifestyle and health indicators

## Technologies Used

* **Python**
* Libraries for data processing and modeling:

  * Python notebook (ipynb) for data analysis and modeling in Google Colab/Jupyter
  * Pandas for data preprocessing and EDA
  * NumPy for numerical computations
  * Scikit-learn for machine learning models
  * SciPy for statistical hypothesis testing
  * Matplotlib and Seaborn for visualizations
  * FastAPI and Uvicorn for API deployment
  * GitHub for reproducibility and version control

## Project Workflow

### 1. Data Preprocessing

* Checked dataset for missing values
* Removed duplicate record inconsistencies
* Validated clinical ranges for features
* Retained meaningful clinical outliers
* Standardized features for Logistic Regression
* Applied stratified train-test split
* Prevented leakage using ML pipelines

### 2. Class Imbalance Handling

* Applied **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset

### 3. Model Development

The following models were implemented and compared:

* Logistic Regression
* Random Forest Classifier
* Other classification approaches (as applicable in notebook)

## Key Insights

* Certain clinical and demographic factors like CRP, vitamin D, ECF/TBW, AST, lean mass %, visceral fat emerged as the strongest predictors of gallstone risk across both statistical tests and machine learning models.
* Logistic Regression (LR) and Random Forest (RF) were selected because they provide the best balance between predictive performance, interpretability, robustness, and suitability for a small clinical dataset.
* Random Forest achieved the strongest overall classification performance demonstrating better generalization and non-linear pattern detection, while Logistic Regression achieved the highest test AUC (0.881) and provided clinically interpretable coefficient-based insights for risk assessment.
* Detailed body-composition metrics captured gallstone risk more effectively than simple BMI-based obesity classification.
* Handling class imbalance improves model reliability and prediction accuracy

## How to Run the Project

1. Clone the repository:

   ```bash
   git clone <your-repo-link>
   ```

2. Navigate to the project folder:

   ```bash
   cd <project-folder>
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

## Project Structure
```
├── data/                    # Dataset files
├── notebooks/               # Jupyter/Colab notebook
├── reports/                 # Synopsis, interim and final reports
├── presentations/           # Presentation deck
└── README.md                # Project documentation
```
## Future Improvements

* Same pipeline can be generalized to a broader family of digestive and metabolic conditions that share overlapping risk factors with gallstone disease
* Integration with real-time clinical systems (EHR - Electronic Health Records system)
* Inclusion of more diverse datasets.

## License

This project is for academic and research purposes.
