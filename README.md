# Group 14 Python Package: Loan Approval Classification (for review)
**Authors**: Reina Cheng Hwai, Edmund Yong, and Joyce Lin

**Link to the report:** [DSCI-522-Group-14-Loan-Approval-Classification](https://github.com/UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification)

## Summary (for review)
Loan Approval Classification is a Python package designed to predict laon approval outcomes and identify the top three customer segments most likely to be approved for a home loan.

Using the train.csv dataset from the [Finance Loan approval Prediction Data](https://www.kaggle.com/datasets/krishnaraj30/finance-loan-approval-prediction-data?select=train.csv) on Kaggle, we fit a classification model to predict loan approval outcomes then analyze which customer groups have the higest predicted approval rates.

This package aims to provide insight into lending patterns by identifying characteristics that may be associated with loan eligibility.

## How to Run the Analysis (unsure)
### 1. Clone the repository
Run the following commands in a Git Bash terminal:

- git clone git@github.com:UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification.git
- cd DSCI-522-Group-14-Loan-Approval-Classification
- uv sync


### 2. Restore the R environment
From an R session started at the top level of the repository:

- renv::restore()

### 3. Build site
From the terminal at the top level of the repository:

- uv run quarto render

## Dependencies (unsure)
- uv
- Quarto
- list them (e.g., uv, Quarto) or link to where they are listed (e.g., pyproject.toml).

## Licenses (TBD)

## AI Use Statement (for review)
Generative AI tools, such as ChatGPT and Claude, were used in this project. AI usage is disclosed in all sections that had assistance. Examples of AI usage include debugging code, answering basic programming questions, asking general concepts, and  proofreading written work.

Examples of prompts include:
- Help me understand why this Python code produced an error?
- What is the difference between predict() and predict_proba()?
- Please proofread this paragraph for grammar and clarity.

#### AI Declaration
This README.md file has been proofread using ChatGPT. Specifically, the Summary and AI Use Statement sections were reviewed by ChatGPT, which provided suggestions for improving clarity and wording.