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

## Sections 6.1 and 6.2: Example Classification Questions (Origianlly labelled by the developers outside the dataset)

The following examples were manually selected by project team members to demonstrate the performance of the Arabic-SBERT & KNN and TF-IDF & SVM classifiers on both long and short Arabic mental health consultation questions.

| Contributor | Model Section | Question Type | Original Category | Question |
|------------|------------|------------|------------|------------|
| Aleen Alzahrani | 6.1 Arabic-SBERT & KNN| Long | Neuropsychological Conditions | تعرضت لحادث سيارة أدى إلى صداع شديد ونوبات تشنجات متكررة، وأصبحت سريعة الخوف من أشياء عادية، مع رعشة في اليدين واضطراب في النوم والأرق، كما تراجع تركيزي وذاكرتي وأدائي في العمل |
| Aleen Alzahrani | 6.1 Arabic-SBERT & KNN | Short | Behavioral Psychological Conditions | يعاني طفلي من سلوك عدواني متكرر؛ إذ يضرب أخته عندما أهتم بها أو أمنحها اهتمامًا |
| Haya Alwuhaibi | 6.1 Arabic-SBERT & KNN | Long | Personality and Self Development | زوجي يستعيض غضبًا معي ومع أفراد أسرته بشكل متكرر، ويشعر أن الناس يكنون له العداء ولا يعاملونه بالإنصاف. وألاحظ أن هذه المشكلة مرتبطة بشخصيته وطريقة تعامله، إذ يعاني من العصبية والغضب السريع، وسرعة الانفعال، وضعف في الثقة بالنفس والتحكم في المزاج |
| Najaf Almohsen | 6.2 TF-IDF & SVM | Long | Psychotic Disorders | أسمع أصواتًا في رأسي تأمرني بأن آذي نفسي، وأشعر أن الناس يراقبونني أو يريدون الإيذاء بي. وأعاني من ضعف في التركيز والذاكرة والنسيان المتكرر، وأحيانًا أنسى الأشياء بسرعة، وأعاني من السرحان وعدم القدرة على الحفظ، مع اضطراب في النوم والأرق، ورعشة، وأحلام مزعجة |
| Najaf Almohsen | 6.2 TF-IDF & SVM | Short | Childhood Psychological Problems | ابني يذهب للروضة، لا يستطيع الجلوس بهدوء لفترة طويلة على مقعدة |
| Haya Alwuhaibi | 6.2 TF-IDF & SVM | Short | Other Psychological and Behavioral Issues | أشعر بالرغبة بإعادة ترتيب الأشياء من حولي دائمًا |
