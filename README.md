# 🎓 Student Performance Prediction Through Machine Learning

> A machine learning project that analyzes student academic and demographic information to predict whether a student is likely to **Pass or Fail**.

## Benstone101 on discord or X (twitter) for help

## 📌 Project Overview

Student performance can be influenced by many factors, including previous grades, study habits, attendance, family background, and other academic and social characteristics.

The goal of this project is to use **Machine Learning** to identify patterns in student data and build models capable of predicting a student's academic outcome.

The project follows a complete machine learning workflow:

**Data Collection → Data Preprocessing → Exploratory Data Analysis → Feature Engineering → Model Training → Model Evaluation → Comparison**

---

## 🎯 Objectives

The main objectives of this project are to:

* Analyze factors that may influence student performance.
* Clean and preprocess real-world student data.
* Convert categorical information into a format suitable for Machine Learning.
* Build multiple classification models.
* Predict whether a student is likely to **Pass or Fail**.
* Compare different Machine Learning algorithms.
* Evaluate model performance using multiple metrics.
* Identify which approach performs best for the given dataset.

---

## 📊 Dataset

This project uses the **UCI Student Performance Dataset**, specifically the `student-mat.csv` dataset.

The dataset contains information about students taking mathematics and includes academic, demographic, family, and social attributes.

### Dataset Characteristics

* **395 students**
* **33 features**
* Numerical and categorical variables
* Academic and demographic information
* Final grade (`G3`) used to determine the student's outcome

### Example Features

| Feature     | Description                         |
| ----------- | ----------------------------------- |
| `age`       | Student's age                       |
| `sex`       | Student's gender                    |
| `school`    | Student's school                    |
| `studytime` | Weekly study time                   |
| `failures`  | Number of previous class failures   |
| `absences`  | Number of school absences           |
| `Medu`      | Mother's education level            |
| `Fedu`      | Father's education level            |
| `goout`     | Frequency of going out with friends |
| `health`    | Current health status               |
| `G1`        | First period grade                  |
| `G2`        | Second period grade                 |
| `G3`        | Final grade                         |

---

## 🧠 Problem Formulation

The original dataset contains a final grade (`G3`) ranging from **0–20**.

For this project, the problem is treated as a **binary classification problem**.

### Target Variable

The final grade is converted into:

* **Pass** → `G3 >= 10`
* **Fail** → `G3 < 10`

This allows the Machine Learning models to answer a simple practical question:

> **"Is this student likely to pass or fail?"**

---

## ⚙️ Data Preprocessing

Before training the models, the dataset goes through several preprocessing steps.

### 1. Data Cleaning

The dataset is inspected for:

* Missing values
* Duplicate records
* Incorrect data types
* Inconsistent categorical values

### 2. Feature Selection

Relevant student attributes are selected for model training while avoiding unnecessary or redundant information.

### 3. Categorical Encoding

Categorical features are converted into numerical representations so that Machine Learning algorithms can process them.

### 4. Feature Scaling

Numerical features are scaled where required, particularly for algorithms such as:

* K-Nearest Neighbors
* Support Vector Machine

### 5. Train/Test Split

The dataset is divided into training and testing sets so that the models can be evaluated on data they have not previously seen.

---

## 🤖 Machine Learning Models

Three classification algorithms are explored in this project.

### 🔹 1. K-Nearest Neighbors (KNN)

KNN predicts the class of a student based on the classes of similar students in the dataset.

It is a simple and intuitive algorithm that can work well when similar students tend to have similar outcomes.

### 🔹 2. Decision Tree

A Decision Tree makes predictions by creating a series of decisions based on the input features.

For example:

```text
Previous Failures?
       │
   ┌───┴───┐
   Yes     No
   │        │
 Fail    Study Time?
            │
        ┌───┴───┐
       Low     High
       │         │
     Fail      Pass
```

Decision Trees are particularly useful because their decisions can be easier to interpret.

### 🔹 3. Support Vector Machine (SVM)

SVM attempts to find the best boundary separating students into the Pass and Fail classes.

It is especially useful when the classes are not easily separated using simple rules.

---

## 📏 Model Evaluation

The models are evaluated using several classification metrics rather than relying only on accuracy.

### Metrics Used

| Metric               | Purpose                                                 |
| -------------------- | ------------------------------------------------------- |
| **Accuracy**         | Overall percentage of correct predictions               |
| **Precision**        | How many predicted cases were actually correct          |
| **Recall**           | How many actual cases were successfully identified      |
| **F1-Score**         | Balance between precision and recall                    |
| **Confusion Matrix** | Detailed breakdown of correct and incorrect predictions |

### Confusion Matrix

The confusion matrix helps visualize:

* True Positives
* True Negatives
* False Positives
* False Negatives

This is particularly useful for understanding where the models make mistakes.

---

## 🔬 Exploratory Data Analysis

Before model training, the dataset is explored to better understand relationships between student characteristics and academic performance.

The analysis investigates factors such as:

* Previous grades
* Study time
* Number of failures
* Absences
* Parental education
* Social activity
* Health
* Family and school-related factors

Visualizations are used to identify patterns, distributions, and potential relationships within the dataset.

---

## 🏗️ Project Workflow

```text
                 ┌─────────────────────┐
                 │   Student Dataset   │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Data Cleaning     │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Data Preprocessing│
                 │ Encoding + Scaling  │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Train / Test Split  │
                 └──────────┬──────────┘
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
          ┌───────┐     ┌──────────┐   ┌─────┐
          │  KNN  │     │ Decision │   │ SVM │
          │       │     │   Tree   │   │     │
          └───┬───┘     └────┬─────┘   └──┬──┘
              │              │             │
              └──────────────┼─────────────┘
                             ▼
                   ┌──────────────────┐
                   │ Model Evaluation │
                   └────────┬─────────┘
                            │
                            ▼
                   ┌──────────────────┐
                   │ Model Comparison │
                   └──────────────────┘
```

---

## 🛠️ Technologies Used

### Programming Language

* **Python**

### Libraries

* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computations
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Scikit-learn** — Machine Learning models and evaluation
* **Jupyter Notebook** — Development and experimentation

---

## 📁 Project Structure

```text
Student-Performance-Prediction-Through-Mchine-Learning/
│
├── data/
│   └── student-mat.csv
│
├── notebooks/
│   └── Student_Performance_Prediction.ipynb
│
├── README.md
│
└── requirements.txt
```

> The exact file structure may vary depending on the current version of the repository.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/sammiullah-gif/Student-Performance-Prediction-Through-Mchine-Learning.git
```

### 2. Navigate to the Project

```bash
cd Student-Performance-Prediction-Through-Mchine-Learning
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the Notebook

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open the project notebook and run the cells sequentially.

---

## 📈 Results

The project compares the performance of:

| Model         | Accuracy | Precision | Recall | F1-Score |
| ------------- | -------: | --------: | -----: | -------: |
| KNN           |        — |         — |      — |        — |
| Decision Tree |        — |         — |      — |        — |
| SVM           |        — |         — |      — |        — |

The final model selection is based on the overall evaluation results rather than accuracy alone.

> **Note:** The exact scores should be added here after the final model evaluation is completed.

---

## 💡 Key Takeaways

This project demonstrates how Machine Learning can be applied to educational data to identify students who may be at risk of failing.

Some important lessons from the project include:

* Student performance is influenced by multiple factors rather than a single variable.
* Data preprocessing is an important part of any Machine Learning project.
* Different algorithms can produce significantly different results on the same dataset.
* Accuracy alone does not always provide a complete picture of model performance.
* Real-world datasets often require careful preparation before they can be used effectively.

---

## 🔮 Future Improvements

Possible improvements include:

* Hyperparameter tuning for each model.
* Testing additional algorithms such as Random Forest, Logistic Regression, and Gradient Boosting.
* Feature importance analysis.
* Handling class imbalance where necessary.
* Using cross-validation for more robust evaluation.
* Developing a web interface for entering student information and receiving predictions.
* Deploying the trained model as an online application.

---

## 👥 Contributors

This project was developed as a collaborative Machine Learning project.

**Team Members:**

* Sammiullah
* *Add other team members here*

---

## 🎓 Academic Project

This project was developed for educational purposes as part of a Machine Learning / Data Science project.

It demonstrates the practical application of:

**Data Analysis → Data Preprocessing → Machine Learning → Model Evaluation → Prediction**

---

## 📄 License

This project is intended primarily for educational and academic use.

---

⭐ **If you find this project useful, consider giving the repository a star!**

