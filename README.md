**ARTI 452 – Natural Language Processing · Group 1**
College of Computer Science & Information Technology, Imam Abdulrahman Bin Faisal University

# Murshed-Mental-Health-Problems-Classifier
---

## Overview
Murshed is an Arabic Natural Language Processing (NLP) system designed to classify (not diagnose) mental health consultation questions into six predefined categories. The system aims to help users identify a relevant mental health support category based on their written questions.

## Repository layout

```
.
├── Murshed.ipynb                           # Complete NLP pipeline: preprocessing, embeddings, training, evaluation, and analysis
├── README.md
├── Dataset/                               # Original Shifaa dataset and category files, must be extracted into the directory locally
│   ├── Behavioral_Psychological_Conditions.csv
│   ├── Childhood_Psychological_Problems.csv
│   ├── Neuropsychological_Conditions.csv
│   ├── Other_Psychological_and_Behavioral_Issues.csv
│   ├── Personality_and_Self_Development.csv
│   ├── Psychological_Issues_and_Guidance.csv
│   ├── Psychotic_Disorders.csv
│   └── Shifaa_Arabic_Mental_Health_Consultations.csv
├── processed_data/                        # Generated during preprocessing
│   ├── embeddings/                        # Sentence embedding files
│   ├── Murshed_Cleaned_Dataset.csv
│   ├── Murshed_Conflicting_Questions.csv
│   ├── Murshed_Dataset.csv
│   ├── Murshed_Train.csv
│   ├── Murshed_Validation.csv
│   └── Murshed_Test.csv
├── .vscode/
├── .ipynb_checkpoints/
└── report/                                
```


## Dataset

The dataset is not redistributed with the code. Download it and place it in the folders shown above. The folder names must match exactly for the notebook to run normally.

| Dataset| Link |
|---|---|
| Shifaa Arabic Mental Health Consultations | https://www.kaggle.com/datasets/ahmedseleem/shifaa-arabic-mental-health-consultations?select=Childhood_Psychological_Problems.csv |

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate            # Windows   (macOS / Linux: source .venv/bin/activate)
pip install -r requirements.txt
```
