# fairness-and-explainability Project 
November 2023

### Introduction
This collaborative project is conducted as part of the **Fairness and Interpretability course**. The primary objective is to apply various techniques covered in the course to a dataset selected by the team. The chosen dataset is related to **education** and focuses on academic performance. We deemed it particularly compelling to work on a dataset related to this domain, as the decision-making processes in education, particularly concerning students, have far-reaching consequences. 

### Goal
The overarching goal of this project is to implement and assess techniques for fairness and interpretability in machine learning models. The target variable is binary, representing whether a student is classified as a good or not good student. The dataset is intentionally chosen to emphasize the importance of interpretability and fairness in the educational domain.

### Dataset Overview
- **Source**: Kaggle (link: https://www.kaggle.com/datasets/desalegngeb/students-exam-scores)
- **Size of the dataset**: 30k rows and 11 Features (Gender, Ethnic Group, Parent Educ, Lunch Type, Test Prep, Parent Marital Status, Practice Sport, Is First Child, Nr Siblings, Transport Means, Wkly Study Hours)
- **Target Variable**: Binary (25% of good student, 75% of bad students)
As a remark, the dataset is balanced regarding gender but not balanced in terms of ethnicity, parent education, and lunch type.

### Project Structure
The repository is organized into folders representing each steps of the process, along with a 'model' folder containing serialized models (pkl format). The main steps are:

1. **Step 1: Exploratory Data Analysis (EDA)**
   - Exploration of the dataset and preprocessing applied.
2. **Step 2: Black-box Model**
   - Implementation of a CatBoost model tailored to specific student groups.
3. **Step 3: Predictive Performance Analysis**
   - Comparison of the black-box model with white-box models. Selected a Generalized Additive Model (GAM) for comparison.
4. **Step 4: Global Interpretability 1**
   - Implementation of a surrogate method (Decision Tree) to interpret the black-box model.
5. **Step 5: Global Interpretability 2**
   - Implementation of two post-hoc global methods (e.g., PDP, ALE) to interpret the black-box model. Comparison with results from Step 4.
6. **Step 6: Local Interpretability**
   - Implementation of two post-hoc local methods (e.g., SHAP, ICE, LIME) to interpret the model. Comparison of results.
7. **Step 7: Performance Interpretability**
   - Decomposition of the preferred performance metric using Permutation Importance and XPER. Comparison of results.
8. **Step 8: Fairness Assessment**
   - Evaluation of the model's fairness with respect to the protected attribute. Statistical tests for Statistical Parity and Conditional Statistical Parity.
9. **Step 9: Fairness-aware Model Post-processing (FPDP)**
   - Implementation of a fairness-aware model post-processing using a fairness measure.
  
### Requirements

This project uses poetry for dependency management. If you haven't installed poetry yet, you can do so by following the instructions on their official documentation: [Poetry Installation Guide](https://python-poetry.org/docs/#installation)

### Setting Up the Environment
1. Clone the repository
```bash
git clone https://github.com/your-username/Tooling-for-data-science-app.git
cd fairness-and-explainability
```
2. Install the dependencies using poetry
```bash
poetry install
```
3. Activate the virtual environment
```bash
poetry shell
```
After following the above steps, you should be inside the virtual environment with all the required packages installed.

## Contributors
- Alvaro Calafell
- Anastasia Nesterova
- Lola Vitrac
- Maxime Gasc
- Christophe Thomassin
