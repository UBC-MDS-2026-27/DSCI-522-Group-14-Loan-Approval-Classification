# Group 14 Milestone 1: Loan Approval Classification (for review)
**Authors**: Reina Cheng Hwai, Edmund Yong, and Joyce Lin

**Link to the report:** [DSCI-522-Group-14-Loan-Approval-Classification](https://github.com/UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification)

## Summary (for review)
The goal of this data analysis project is to predict loan approval outcomes and identify the top three customer segments most likely to be approved for a home loan.

Using the train.csv dataset from the [Finance Loan approval Prediction Data](https://www.kaggle.com/datasets/krishnaraj30/finance-loan-approval-prediction-data?select=train.csv) on Kaggle, we fit a classification model to predict loan approval outcomes then analyze which customer groups have the higest predicted approval rates.

This analysis aims to provide insight into lending patterns by identifying characteristics that may be associated with loan eligibility.

## How to Run the Analysis (unsure)
### 1. Clone the repository
Run the following commands in a Git Bash terminal:

- git clone git@github.com:UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification.git
- cd DSCI-522-Group-14-Loan-Approval-Classification

### 2. Set up the Python environment
From the root of the repository, run:
- uv sync

This creates the project's virutal environment and installs the dependencies specified in uv.lock.

### 3. Download the dataset
Run the following command in the root of the project repository:

`curl -L -o data/finance-loan-approval-prediction-data.zip https://www.kaggle.com/api/v1/datasets/download/krishnaraj30/finance-loan-approval-prediction-data && \ unzip -o data/finance-loan-approval-prediction-data.zip -d data/raw/ && \ rm data/finance-loan-approval-prediction-data.zip data/raw/test.csv`


### 4. Run the analysis
TBC

## Dependencies (unsure)
- Git
- Python (managed through uv)
- uv
- Quarto

Python package dependencies are listed in pyproject.toml, with resolved versions recorded in uv.lock.


## Licenses
 This software is dual-licensed under the MIT License and the CC BY-NC-ND 4.0 License


## AI Use Statement (for review)
Generative AI tools, such as ChatGPT and Claude, were used in this project. AI usage is disclosed in all sections that had assistance. Examples of AI usage include debugging code, answering basic programming questions, asking general concepts, and  proofreading written work.

Examples of prompts include:
- Help me understand why this Python code produced an error?
- What is the difference between predict() and predict_proba()?
- Please proofread this paragraph for grammar and clarity.

#### AI Declaration
All this README.md file has been proofread using ChatGPT. Specifically, the Summary, AI Use Statement, How to Run the Analysis, and Dependicies were proofread and reviewed by ChatGPT where it provided suggestions for improving clarity and wording.