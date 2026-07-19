# 🩺 Thyroid Disease Prediction Using Machine Learning

A Machine Learning project that predicts the presence of thyroid disease using patient medical data and laboratory test results. This project applies data preprocessing, missing value handling, feature engineering, and classification algorithms to accurately identify thyroid disorders.

---

## 📌 Overview

Thyroid disorders are among the most common endocrine diseases worldwide. Early detection can significantly improve treatment outcomes. This project uses Machine Learning techniques to classify patients as thyroid-positive or thyroid-negative based on clinical and laboratory parameters.

The project implements and compares the performance of three machine learning algorithms:

- Decision Tree Classifier (DTC)
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

Among these models, the Decision Tree Classifier achieved the highest accuracy and was selected for final prediction.

---

## 🎯 Objectives

- Predict thyroid disease using patient health records.
- Compare different machine learning classification algorithms.
- Evaluate model performance using accuracy scores and confusion matrices.
- Develop a simple prediction system for new patient data.

---

## 📊 Dataset Description

The dataset contains various medical and thyroid-related attributes collected from patients.

### Input Features

- age
- sex
- on thyroxine
- query on thyroxine
- on antithyroid medication
- sick
- pregnant
- thyroid surgery
- I131 treatment
- query hypothyroid
- query hyperthyroid
- lithium
- goitre
- tumor
- hypopituitary
- psych
- TSH
- T3
- TT4
- T4U
- FTI

### Target Variable

**binaryClass**

- 0 → Negative (No Thyroid Disease)
- 1 → Positive (Thyroid Disease)

---

## 🛠 Data Preprocessing

### Handling Missing Values

The dataset contained missing values represented by "?".

These values were:

1. Replaced with NaN.
2. Filled using Mean Imputation through Scikit-Learn's `SimpleImputer`.

### Categorical Encoding

The following conversions were performed:

```text
P → 0
N → 1

M → 1
F → 2

t → 1
f → 0
```

### Removed Columns

The following columns were removed because they were unnecessary or contained excessive missing values:

```text
TBG
TBG measured
referral source
TSH measured
T3 measured
TT4 measured
T4U measured
FTI measured
```

---

## ⚙️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib

---

## 🧠 Machine Learning Models

### 1. Decision Tree Classifier

```python
from sklearn.tree import DecisionTreeClassifier

dtcmodel = DecisionTreeClassifier()
dtcmodel.fit(x_train, y_train)
```

### Accuracy

```text
99.73%
```

---

### 2. K-Nearest Neighbors (KNN)

```python
from sklearn.neighbors import KNeighborsClassifier

knmodel = KNeighborsClassifier(n_neighbors=3)
knmodel.fit(x_train, y_train)
```

### Accuracy

```text
95.10%
```

---

### 3. Support Vector Machine (SVM)

```python
from sklearn.svm import SVC

svcmodel = SVC()
svcmodel.fit(x_train, y_train)
```

### Accuracy

```text
94.43%
```

---

## 📈 Model Performance Comparison

| Algorithm | Accuracy |
|------------|------------|
| Decision Tree Classifier | 99.73% |
| K-Nearest Neighbors | 95.10% |
| Support Vector Machine | 94.43% |

### ✅ Best Model

**Decision Tree Classifier**

Final Accuracy:

```text
99.73%
```

The Decision Tree model significantly outperformed the other models and was selected for deployment in the prediction system.

---

## 📊 Visualization

### Accuracy Comparison Graph

A bar chart was generated using Matplotlib to compare the performance of the three algorithms.

The graph shows:

- Decision Tree Classifier achieved the highest accuracy.
- KNN produced competitive results.
- SVM delivered satisfactory but comparatively lower performance.

---

### Confusion Matrix

A confusion matrix was generated for the Decision Tree Classifier to evaluate classification performance.

The matrix helps analyze:

- True Positives
- True Negatives
- False Positives
- False Negatives

This provides deeper insight into how well the model classifies thyroid-positive and thyroid-negative patients.

---

## 🔍 Prediction System

The trained Decision Tree model can predict whether a patient has thyroid disease based on user-provided input values.

### Example Input

```text
45,1,0,0,0,0,0,0,0,1,0,0,0,0,0,0,2.1,1.8,120,1.1,110
```

### Example Output

```text
Male
Not Pregnant
Negative
```

or

```text
Female
Pregnant
Positive
```

---

## 🚀 Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/Thyroid-Disease-Prediction.git
cd Thyroid-Disease-Prediction
```

### Install Required Libraries

```bash
pip install pandas numpy matplotlib scikit-learn
```

---

## ▶️ Run the Project

```bash
python thyroid_prediction.py
```

---

## 📦 Required Libraries

```text
pandas
numpy
matplotlib
scikit-learn
```

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

## 📁 Project Structure

```text
Thyroid-Disease-Prediction/
│
├── thyroid.csv
├── thyroid_prediction.py
├── README.md
├── requirements.txt
│
├── images/
│   ├── accuracy_graph.png
│   ├── confusion_matrix.png
│
└── outputs/
    └── prediction_results.txt
```

---

## 🔮 Future Enhancements

- Hyperparameter tuning for improved model performance.
- Feature importance analysis.
- Cross-validation techniques.
- Model deployment using Flask.
- Interactive web application using Streamlit.
- Real-time prediction dashboard.
- Integration with healthcare management systems.

---

## 📚 Learning Outcomes

Through this project, the following concepts were explored:

- Data Cleaning
- Missing Value Imputation
- Data Preprocessing
- Feature Selection
- Classification Algorithms
- Model Evaluation
- Data Visualization
- Machine Learning Workflow

---

## 👨‍💻 Author

**Aatharsh B**

Engineer | Machine Learning Enthusiast

GitHub: https://github.com/your-username

---

## ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub to support the project and encourage future development.

---

## 📄 License

This project is licensed under the MIT License.

Feel free to use, modify, and distribute this project for educational and research purposes.
