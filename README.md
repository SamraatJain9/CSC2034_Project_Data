---


<h3 align="center"> CSC2034 repository for Data Science - Wine Quality Prediction! This README will help you get started with cloning, setting up, and running the project.
</h3>

---

# CSC2034 Final Report/Product, Data Science 2024/25

# Setup:
- Create a virtual environment - ```python -m venv venv```
- Source into the virtual environment ```venv\Scripts\activate``` (for windows powershell)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Installation](#installation)
3. [How to Run](#how-to-run)
4. [Contributors](#Contributors)
5. [License](#license)

---

## Project Overview
This project involved consulting for a Portuguese winery that produces traditional "Vinho Verde" wines. The objective was to analyze the chemical properties of red and white wines to identify the key factors that influence wine quality, with the ultimate goal of optimizing production processes.

Three datasets were used. All are present inside the wine_data folder:

- winequality-red.csv – 1,599 samples of red wine.

- winequality-white.csv – 4,898 samples of white wine.

- winequality.names – A metadata file describing the 12 variables included in each sample.

Each data point consisted of 11 physicochemical features (e.g., acidity, sugar content, pH) and one target variable representing sensory quality, scored between 0 and 10.

Project Goals:
- Perform Exploratory Data Analysis (EDA) to examine distributions, detect outliers, and understand relationships between features.

- Preprocess the data, including scaling and encoding where necessary.

- Train and evaluate machine learning models such as Random Forest, Support Vector Machines, and XGBoost.

- Interpret model outputs to determine which features most strongly impact perceived wine quality.

## Summary

Key Predictive Features for Wine Quality:
- Alcohol
- Density
- Volatile Acidity
- Chlorides
- Citric acid
- Fixed Acidity

Recommended Threshold: 
Threshold 6 offers the best trade-off between class balance and predictive performance across models, making it a practical cutoff for binary quality classification.

## Results

========== XGBoost Summary ==========

Threshold: 5
  → Accuracy : 0.95
  → F1 Score : 0.98
  → AUC      : 0.72

Threshold: 6
  → Accuracy : 0.73
  → F1 Score : 0.79
  → AUC      : 0.78

Threshold: 7
  → Accuracy : 0.82
  → F1 Score : 0.41
  → AUC      : 0.81

Threshold: 9
  → Accuracy : 1.00
  → F1 Score : 0.00
  → AUC      : 0.45

========== Support Vector Machine Summary ==========

Threshold: 5
  → Accuracy : 0.96
  → F1 Score : 0.98
  → AUC      : 0.61

Threshold: 6
  → Accuracy : 0.73
  → F1 Score : 0.79
  → AUC      : 0.79

Threshold: 7
  → Accuracy : 0.81
  → F1 Score : 0.00
  → AUC      : 0.72

Threshold: 9
  → Accuracy : 1.00
  → F1 Score : 0.00
  → AUC      : 0.77

========== Random Forest Summary ==========

Threshold: 5
  → Accuracy : 0.95
  → F1 Score : 0.98
  → AUC      : 0.64

Threshold: 6
  → Accuracy : 0.75
  → F1 Score : 0.81
  → AUC      : 0.70

Threshold: 7
  → Accuracy : 0.82
  → F1 Score : 0.37
  → AUC      : 0.73

Threshold: 9
  → Accuracy : 1.00
  → F1 Score : 0.00
  → AUC      : 0.45

========== Tuned Random Forest Summary ==========

Threshold: 5
  → Accuracy : 0.95
  → F1 Score : 0.98
  → AUC      : 0.73

Threshold: 6
  → Accuracy : 0.75
  → F1 Score : 0.80
  → AUC      : 0.79

Threshold: 7
  → Accuracy : 0.82
  → F1 Score : 0.38
  → AUC      : 0.82

Threshold: 9
  → Accuracy : 1.00
  → F1 Score : 0.00
  → AUC      : 0.49

---

## Installation

1. **Clone the Repository**  
   Begin by cloning the repository from GitHub (SSH):
   ```bash
   git clone git@github.com:SamraatJain9/CSC2034_Project_Data.git
2. **Navigate to the project folder**  
   ```bash
   cd CSC2034_Project_Data
3. **Install Dependencies**  
   Use the following command to install all necessary dependencies from [requirements.txt](requirements.txt):
   ```bash
   pip install -r requirements.txt
---

## How to Run

1. **Launch the Jupyter Notebook**  
   Start Jupyter Notebook from your terminal:
   ```bash
   jupyter notebook
   ```
   This will open a browser window with the Jupyter interface. Navigate to the notebook file **main.ipynb** and open it.

2. **Run the Notebook**  
   - Click Kernel > Restart & Run All to ensure all cells execute in the correct order.
   - Wait for the notebook to finish running. It may take a few moments depending on your system and the models used.

---

## Contributors
The contributor(s) of this project: [Samraat Jain](https://github.com/SamraatJain9).

## License
License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.