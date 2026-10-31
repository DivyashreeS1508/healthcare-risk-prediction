# Healthcare Risk Prediction Using Machine Learning

## Project Overview
This project explores machine learning techniques for predicting health-related outcomes using publicly available datasets. It examines diabetes, hypertension, and mental health data as separate prediction tasks.

## Objectives
- Load and inspect healthcare datasets.
- Clean data and handle missing values.
- Preprocess numerical and categorical features.
- Compare a majority-class baseline with a Random Forest classifier.
- Evaluate models using accuracy, precision, recall, F1-score, and ROC-AUC where applicable.

## Datasets
The project is designed to work with these CSV files:
- `diabetes.csv` — target: `Outcome`
- `hypertension_dataset.csv` — target: `Hypertension`
- `Mental Health Dataset.csv` — target: `treatment`

Place the files in a local `datasets` folder. Do not upload private or restricted data to GitHub.

## Tools and Technologies
- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## How to Run
1. Install the packages listed in `requirements.txt`.
2. Place the required CSV files in the local `datasets` folder.
3. Open the notebook in Jupyter or VS Code.
4. Run the notebook cells in order.

## Important Limitations
The datasets do not share verified patient identifiers, so they are analysed separately rather than combined into synthetic patient records. Results are exploratory and are not intended for medical diagnosis or clinical decision-making.

## Author
MCA graduate specializing in Artificial Intelligence and Data Science.
  
  ## Preliminary Model Results

The models were evaluated separately for each dataset using a majority-class baseline and a Random Forest classifier.

| Dataset | Model | Accuracy | Balanced Accuracy | ROC-AUC |
|---|---|---:|---:|---:|
| Diabetes | Baseline | 64.94% | 50.00% | 0.5000 |
| Diabetes | Random Forest | 77.27% | 73.56% | 0.8220 |
| Hypertension | Baseline | 71.90% | 50.00% | 0.5000 |
| Hypertension | Random Forest | 71.89% | 49.99% | 0.4980 |
| Mental Health | Baseline | 50.60% | 50.00% | 0.5000 |
| Mental Health | Random Forest | 73.08% | 73.08% | 0.7971 |

### Findings
- **Diabetes:** Random Forest outperformed the baseline on accuracy, balanced accuracy, and ROC-AUC.
- **Hypertension:** Random Forest did not meaningfully outperform the baseline. Its ROC-AUC was approximately 0.50, indicating performance near chance level.
- **Mental health:** Random Forest outperformed the baseline on the evaluated sample.

### Limitations
The hypertension results indicate that further investigation of the labels, features, and data quality is needed. The hypertension and mental-health models were evaluated on samples of 50,000 rows; results may vary with different samples and splits. These are exploratory educational experiments, not clinically validated models. They must not be used for medical diagnosis or treatment decisions.
