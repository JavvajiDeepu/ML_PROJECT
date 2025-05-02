#### Student Exam Performance Prediction

### Objective:
Objective of this project is to predict results of test that are performed by students, based on Gender, race_ethnicity, parental_level_of_education, lunch type, test_preparation_course, math score, reading score, writing score.

### Tech Stack
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)  ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)  ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)  ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)  ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white) ![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)

#### Project structure

    .
    ├───.ebextensions
    ├───artifacts
    │   ├───data.csv
    │   │    ├─── model.pkl
    │   │    └─── preprocessor.pkl
    │   ├─── test.csv
    │   └─── train.csv
    │
    ├───catboost_info
    │   ├───learn
    │   └───tmp
    ├───logs
    │   ├───03_21_2025_19_03_19_48.log
    ├───notebook
    │   ├───catboost_info
    │   │   ├───learn
    │   │   └───tmp
    │   └───data
    │       ├─── stud.csv
    │       ├─── EDA STUDENT PERFORMANCE.ipynb
    │       └─── MODEL TRAINING.ipynb
    ├───Scripts
    ├───src
    │   ├───components
    │   │   │───__pycache__
    │   │   │─── __init__.py
    │   │   │─── data_ingestion.py     
    │   │   │─── data_transformation.py
    │   │   └─── model_trainer.py
    │   ├───pipeline
    │   │    │─── __init__.py
    │   │    │───__pycache__
    │   │    │─── predict_pipeline.py
    │   │    └─── train_pipeline.py  
    │   │───__init__.py
    │   │─── exception.py
    │   │─── logger.py  
    │   └───utils.py
    ├───templates
    │    │───home.html
    │    └───index.html
    │─── .gitignore
    │─── appy.py
    │───application.py
    └───Readme.md

#### Implementation:

1. Data source: Datasets for training of this model were taken from Kaggle, here is the link:https://www.kaggle.com/code/nitindatta/students-performance-in-exams-eda-in-depth

2.