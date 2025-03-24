# ml-project-premium-prediction
 health insurance prediction project

# Healthcare Premium Prediction

## Overview
This repository contains a project aimed at predicting healthcare insurance premiums using advanced machine learning techniques. The dataset includes various features such as age, BMI, and smoking status to predict insurance premiums accurately.

## Motivation and Goals
The motivation behind this project is to provide a tool for predicting healthcare insurance premiums accurately and efficiently, thereby helping both insurers and customers. The goals include:
- Building a robust predictive model.
- Reducing errors in premium predictions, especially for specific age groups.
- Ensuring interpretability and reliability of the models.

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
XGBoost was chosen for its ability to handle tabular data efficiently and its strong performance with tree-based methods. The following models were trained and evaluated:
- A single model for the entire dataset.
- Separate models for individuals under 25 and those 25 and older, both with and without the `Genetical_Risk` column.

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
- Deploying the app on a cloud platform for broader accessibility.

---

Feel free to contribute or raise issues for further improvements!



