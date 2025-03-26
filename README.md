
# Healthcare Premium Prediction

## Overview
This repository contains a project aimed at predicting healthcare insurance premiums using advanced machine learning techniques. The dataset includes various features such as age, BMI, and smoking status to predict insurance premiums accurately.

---

![Project Screenshot](image 1/Screenshot (97).png)

## Motivation

Health insurance is a critical component of financial planning, and setting premiums is a complex process influenced by multiple factors. Accurate prediction of premiums:

- Enhances transparency in the insurance industry.
- Helps companies optimize their pricing strategies.
- Empowers customers to make informed decisions.

This project addresses these needs using data-driven approaches to predict premiums based on historical data.

---

## Goals

The primary objectives of this project are:

1. **Develop a machine learning pipeline** to predict health insurance premiums accurately.
2. **Understand the influence of key features** (e.g., age, BMI, smoking habits) on premium costs.
3. **Provide an explainable model** that aids decision-making for both insurers and policyholders.

---

## Project Structure
The project is organized into the following main components:

### 1. **Main Files**
- `main.py`: A script designed to help deploy the model as a Streamlit app for user-friendly premium prediction.
- `prediction_helper.py`: This file assists in selecting the appropriate model based on the user’s input, such as age.

### 2. **Artifacts**
- The `artifacts/` folder contains pre-trained models and scaling objects used during predictions.

### 3. **Code**
The `code/` folder contains scripts and notebooks used for model development. The presence of multiple files is explained by the iterative approach taken to improve predictions:

- **Motivation for Multiple Files**: Initially, the model showed high errors for individuals under 25 years old, even when overall accuracy was good. To address this, a new column, `Genetical_Risk`, was introduced, significantly reducing errors for this age group.

- **Files Explanation**:
  - `ml_premium_prediction.ipynb`: Training and evaluation code for the entire dataset without the `Genetical_Risk` column.
  - `ml_premium_prediction_young.ipynb`: Code for training a model specifically for individuals under 25 without the `Genetical_Risk` column.
  - `ml_premium_prediction_young_with_gr.ipynb`: Code for individuals under 25 with the `Genetical_Risk` column.
  - `ml_premium_prediction_rest.ipynb`: Code for individuals 25 and older without the `Genetical_Risk` column.
  - `ml_premium_prediction_rest_with_gr.ipynb`: Code for individuals 25 and older with the `Genetical_Risk` column.

## Technical Aspects

### Model Selection

Multiple models were evaluated during this project, including:

Linear Regression: Initially tested for its simplicity, but it failed to capture non-linear relationships.

XGBoost: Selected for its ability to model non-linear relationships effectively and achieve high accuracy across various subsets of data.

### Libraries and Tools
- **Python**: Programming language for all scripts and notebooks.
- **Libraries**: pandas, NumPy, scikit-learn, XGBoost, Streamlit.
- **Tools**: Jupyter Notebook for development and analysis, Streamlit for deployment.

For more details on data cleaning, feature engineering techniques, model training, and evaluation, refer to the notebooks in the `code/` folder.

---

## Setup

### Dependencies Installation
Ensure you have Python installed. Clone the repository and run the following commands to install dependencies:

```bash
# Clone the repository
git clone https://github.com/NDN-Surya/Healthcare-Premium-Prediction.git

# Navigate to the project directory
cd Healthcare-Premium-Prediction

# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# For Windows
venv\Scripts\activate
# For Mac/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### Running the App
To start the Streamlit app:

```bash
streamlit run app/main.py
```

---

## Future Enhancements
- Expanding the dataset for better generalization.
- Incorporating additional features to improve model accuracy.

---

Feel free to contribute or raise issues for further improvements!



