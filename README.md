# Healthcare Consultation Mode Predictor
  

## Project Overview
This repository contains a full-stack Data Science solution to predict patient consultation modes (**Teleconsultation** vs. **In-Person**) using the [Kaggle Healthcare Dataset](https://www.kaggle.com/datasets/prasad22/healthcare-dataset).

## Repository Structure
- `teleconsultation_predictor.ipynb`: Main Jupyter Notebook containing EDA, Visualizations, and ML Modeling.
- `report.md`: Detailed technical report for panel presentation.
- `healthcare_dataset.csv`: The raw dataset used for training/testing.
- `cleaned_healthcare_dataset.csv`: Processed dataset with engineered features.
- `vox_01...09_*.png`: High-resolution visualizations generated during analysis.

## Technical Requirements
To run this project, install the following dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Methodology Highlights
- **Engineered Triage Logic**: Clinical rule-based target variable with added stochastic noise for realism.
- **Multi-Model Comparison**: Evaluated Logistic Regression, Decision Tree, and Random Forest.
- **Robust Evaluation**: Used 80/20 stratified split and 5-fold cross-validation.
- **Comprehensive Visuals**: 9 detailed plots covering everything from feature correlation to model performance.

## Final Model Performance
- **Primary Model**: Random Forest Classifier
- **Accuracy**: ~96.8%
- **Top Predictors**: Admission Type, Medical Condition, Test Results.

## How to Run
1. Open the directory in your terminal.
2. Ensure `healthcare_dataset.csv` is present.
3. Launch Jupyter: `jupyter notebook teleconsultation_predictor.ipynb`.
4. Run all cells to see output and visualizations.
