# Group 14 Milestone 1: Home Loan Approval Classification
**Authors**: Reina Cheng Hwai, Edmund Yong, and Joyce Lin

**Link to the report:** [DSCI-522-Group-14-Loan-Approval-Classification](https://github.com/UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification)

## Summary
The goal of this data analysis project is to predict home loan approval outcomes using applicant information and evaluate the effectiveness of a machine learning classification model. Using the train.csv dataset from the [Finance Loan Approval Prediction Data]( https://www.kaggle.com/datasets/krishnaraj30/finance-loan-approval-prediction-data?select=train.csv) on Kaggle, we fit a logistic regression model and compare its performance against a majority-class baseline using accuracy, F1 score, and ROC AUC. Our findings show that logistic regression outperforms the baseline, but despite its relatively high overall accuracy, the model performs poorly at identifying rejected applications. This analysis highlights the importance of evaluating classification models beyond overall accuracy, particularly when working with imbalanced datasets, and suggests that further improvements are needed before such a model could be considered for real-world lending decisions.

## How to Run the Analysis
### 1. Clone the repository
Run the following commands in a Git Bash terminal:

```bash
git clone git@github.com:UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification.git
cd DSCI-522-Group-14-Loan-Approval-Classification
```

### 2. Set up the Python environment
From the root of the repository, run:

```bash
uv sync
```

This creates the project's virutal environment and installs the dependencies specified in uv.lock.

### 3. Access the dataset
The datasets train.csv and test.csv are already included in the repository under data/raw/ and do not require a separate download.

The original dataset is available on Kaggle: [Finance Loan Approval Prediction Data](https://www.kaggle.com/datasets/krishnaraj30/finance-loan-approval-prediction-data).

The analysis uses train.csv to train and evaluate the classification model. The test.csv file is included but is not used for model evaluation because it does not contain the target variable, Loan_Status.


### 4. Run the analysis

The Quarto source file (.qmd) contains the analysis code and report. You can open this file in a text editor to review or modify the analysis.

From the root of the repository, run one of the following commands to execute the analysis and generate a report.

**To generate an HTML report:**

```bash
quarto render analysis/loan_classification_report.qmd --to html
```

**To generate a PDF report:**

```bash
quarto render analysis/loan_classification_report.qmd --to pdf
```

## Dependencies
- Git
- Python (managed through uv)
- uv
- Quarto

Python package dependencies are listed in pyproject.toml, with resolved versions recorded in uv.lock.


## Licenses
 This software is dual-licensed under the MIT License and the CC BY-NC-ND 4.0 License


## AI Use Statement
Generative AI tools, such as ChatGPT and Claude, were used in this project. AI usage is disclosed in all sections that had assistance. Examples of AI usage include debugging code, answering basic programming questions, asking general concepts, and  proofreading written work.

Examples of prompts include:
- Help me understand why this Python code produced an error?
- What is the difference between predict() and predict_proba()?
- Please proofread this paragraph for grammar and clarity.

## AI Declaration
All this README.md file has been proofread using ChatGPT. Specifically, the Summary, AI Use Statement, How to Run the Analysis, and Dependencies were proofread and reviewed by ChatGPT where it provided suggestions for improving clarity and wording.

## REFERENCES
This document was developed following the instructions and recommended workflows presented in the following resources:
- Sheng, K., Foris, B., Weary, D., & von Keyserlingk, M. (n.d.). moo4feed [Computer software]. GitHub. [https://github.com/skysheng7/moo4feed](https://github.com/skysheng7/moo4feed)
- University of British Columbia, Master of Data Science Program. (n.d.). Milestone 1. DSCI 522: Data Science Workflows (Students). [https://ubc-mds.github.io/DSCI_522_dsci-workflows_students/assignments/milestone1.html](https://ubc-mds.github.io/DSCI_522_dsci-workflows_students/assignments/milestone1.html)