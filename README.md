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

2.This project is inspired by the growing need in educational systems to use data-driven approaches to support student success. Teachers and educational institutions often struggle to recognize early signs of academic difficulties, especially when they are influenced by complex socioeconomic or background factors. Through machine learning, this project seeks to provide valuable insights into which students might be at risk and why—helping educators create personalized learning strategies or interventions.

The dataset used contains multiple records of students along with their exam scores and background information. After loading the data, the first step was to perform data cleaning and preprocessing. This involved checking for missing values, correcting data types, and transforming categorical variables into numerical formats using encoding techniques such as one-hot encoding or label encoding. Numerical features such as exam scores were also explored for outliers and distribution patterns.

Next, exploratory data analysis (EDA) was performed to gain insights into relationships between variables. Visualizations were used to observe the impact of gender, race, parental education, and lunch types on test scores. It was observed that students who completed the test preparation course generally performed better, and students with parents who had higher levels of education tended to score higher. These insights helped in selecting and engineering the most relevant features for the prediction model.

The dataset was then split into training and testing sets to evaluate model performance on unseen data. Several machine learning models were trained, including Logistic Regression, Decision Tree, Random Forest, Gradient Boosting, Support Vector Machine, and others. For regression tasks (e.g., predicting total or average scores), models like Linear Regression and XGBoost Regressor were also evaluated. The performance of each model was assessed using appropriate evaluation metrics—such as accuracy, precision, recall, and F1-score for classification tasks, and R² score, Mean Absolute Error (MAE), and Mean Squared Error (MSE) for regression tasks.

The model that achieved the best performance based on these metrics was selected and saved using serialization techniques like pickle or joblib. This model can now be reused in production environments or integrated into a web application.

As part of deployment, the model was optionally integrated into a user-friendly interface using a web framework such as Flask or Streamlit. This allowed users—such as teachers or school administrators—to input student information and receive immediate predictions about expected academic performance. The application was designed to run either locally or on a cloud platform such as AWS EC2 for broader access.

#### In conclusion:
The Student Performance Prediction project demonstrates how machine learning can be effectively used in education to provide predictive insights. It not only helps identify students who may need additional academic attention but also sheds light on how socio-economic and preparatory factors influence academic outcomes. Future improvements may include incorporating behavioral data, attendance records, or even psychological metrics to further refine predictions and enhance model interpretability.

