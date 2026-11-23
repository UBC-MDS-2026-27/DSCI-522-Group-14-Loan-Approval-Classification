# Group 14 Milestone 1: Predicting Home Loan Approvals Given An Applicant Financial And Application Details
**Authors**: Reina Cheng Hwai, Edmund Yong, and Joyce Lin

**Link to the report:** [DSCI-522-Group-14-Loan-Approval-Classification](https://github.com/UBC-MDS-2026-27/DSCI-522-Group-14-Loan-Approval-Classification)

## Summary
The goal of this data analysis project is to predict home loan approval outcomes using applicant information and evaluate the effectiveness of a machine learning classification model. Using the train.csv dataset from the [Finance Loan Approval Prediction Data]( https://www.kaggle.com/datasets/krishnaraj30/finance-loan-approval-prediction-data?select=train.csv) on Kaggle, we fit a logistic regression model and compare its performance against a majority-class baseline using accuracy, F1 score, and ROC AUC. Our findings show that logistic regression outperforms the baseline, but despite its relatively high overall accuracy, the model performs poorly at identifying rejected applications. This analysis highlights the importance of evaluating classification models beyond overall accuracy, particularly when working with imbalanced datasets, and suggests that further improvements are needed before such a model could be considered for real-world lending decisions.

## Report

The final report can be found
[here](https://ubc-mds-2026-27.github.io/DSCI-522-Group-14-Loan-Approval-Classification/analysis/loan_classification_report.html).

## Usage

We run the analysis in a Docker container,
so everyone uses the same software and package versions.
The image is published on Docker Hub at
[skysheng7/dsci_522_project-template-breast-cancer-predictor](https://hub.docker.com/r/skysheng7/dsci_522_project-template-breast-cancer-predictor).

### Setup

First time running the project,
install and launch [Docker](https://www.docker.com/get-started/),
then clone this repository and move into it:

``` bash
git clone https://github.com/UBC-MDS/DSCI_522_project-template-breast-cancer-predictor.git
cd DSCI_522_project-template-breast-cancer-predictor
```

Run all the commands below from the root of this repository.

### 1. Make an ssh key

If you don't have an ssh key yet, make one
and press Enter at each question:

``` bash
ssh-keygen -t ed25519
```

The container lets you log in with this key.
If you skip this step, Docker makes a *folder* named `~/.ssh/id_ed25519.pub` instead,
and connecting to the container over ssh fails
until you delete that folder and make the key.

### 2. Download the image

``` bash
docker compose pull
```

### 3. Run the analysis and render the report

``` bash
docker compose run --rm analysis-env uv run quarto render
```
The container stops with `--rm`; it is removed by itself when the render finishes.

Rendering runs the whole analysis from scratch:
it downloads the data again from the UCI Machine Learning Repository
(so you need an internet connection),
and overwrites the files in `data/raw/` and `data/processed/`.
The rendered report is written to
`reports/breast_cancer_predictor_report.html` and
`reports/breast_cancer_predictor_report.pdf`,
replacing the versions in this repository.
Because of `--rm`, the container is removed by itself
when the render finishes, so there is nothing to stop afterwards.


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

### 3. Download the dataset
The following command downloads and unzips the dataset into `data/raw/`.

```bash
curl -L -o data/finance-loan-approval-prediction-data.zip https://www.kaggle.com/api/v1/datasets/download/krishnaraj30/finance-loan-approval-prediction-data && \
unzip -o data/finance-loan-approval-prediction-data.zip -d data/raw/ && \
rm data/finance-loan-approval-prediction-data.zip
```

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

## Contributing

Want to change the analysis, add a package, or update the published report?
See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## AI Use Statement
Generative AI tools, such as ChatGPT and Claude, were used in this project. AI usage is disclosed in all documents that had assistance. Examples of AI usage include debugging code, answering basic programming questions, asking general concepts, and  proofreading written work.

Examples of prompts include:
- Help me understand why this Python code produced an error?
- What is the difference between predict() and predict_proba()?
- Please proofread this paragraph for grammar and clarity.

## AI Declaration
This README.md file has been proofread using ChatGPT. Specifically, the Summary, AI Use Statement, How to Run the Analysis, and Dependencies were proofread and reviewed by ChatGPT where it provided suggestions for improving clarity and wording.

## REFERENCES
This document was developed following the instructions and recommended workflows presented in the following resources:
- Sheng, K., Foris, B., Weary, D., & von Keyserlingk, M. (n.d.). moo4feed [Computer software]. GitHub. [https://github.com/skysheng7/moo4feed](https://github.com/skysheng7/moo4feed)
- University of British Columbia, Master of Data Science Program. (n.d.). Milestone 1. DSCI 522: Data Science Workflows (Students). [https://ubc-mds.github.io/DSCI_522_dsci-workflows_students/assignments/milestone1.html](https://ubc-mds.github.io/DSCI_522_dsci-workflows_students/assignments/milestone1.html)
