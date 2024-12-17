
---

## **Kaggle의 Titanic Dataset 분석**

```markdown
# 🚢 Titanic - Machine Learning from Disaster

Predicting survival on the Titanic using machine learning.

---

## 📖 **Overview**
This project is based on the Kaggle competition ["Titanic: Machine Learning from Disaster"](https://www.kaggle.com/competitions/titanic). The goal is to predict whether a passenger survived or not based on features like age, gender, class, and more.

---

## 📊 **Dataset Description**
The dataset contains the following files:
- **train.csv**: Training data with survival labels (`Survived`).
- **test.csv**: Testing data for which survival predictions are to be made.

### **Features**
- `PassengerId`: Unique ID for each passenger
- `Survived`: Survival indicator (0 = No, 1 = Yes)
- `Pclass`: Ticket class (1st, 2nd, 3rd)
- `Name`: Passenger's name
- `Sex`: Gender
- `Age`: Age of passenger
- `SibSp`: Number of siblings/spouses aboard
- `Parch`: Number of parents/children aboard
- `Ticket`: Ticket number
- `Fare`: Passenger fare
- `Cabin`: Cabin number
- `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

---

## 🚀 **How to Run the Project**
### **1. Prerequisites**
Make sure the following libraries are installed:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm
```

### **2. Running the Code**
- Use the provided **Jupyter Notebook**: `titanic.ipynb`
- Follow the steps:
  1. Load the data
  2. Preprocess and clean the data
  3. Feature engineering
  4. Model training and evaluation
  5. Prediction and submission

To run the notebook, execute the following command:
```bash
jupyter notebook titanic.ipynb
```

---

## 🛠 **Methodology**
### **1. Data Preprocessing**
- Handle missing values (`Age`, `Embarked`, `Fare`, `Cabin`)
- Encode categorical variables (`Sex`, `Embarked`, `Title`)
- Create new features: `FamilySize`, `IsAlone`

### **2. Model Selection**
The following models were tested:
- **Random Forest**
- **Gradient Boosting**
- **XGBoost**
- **LightGBM**

### **3. Ensemble Model**
A **Soft Voting Classifier** combining Random Forest, Gradient Boosting, XGBoost, and LightGBM was used for final predictions.

---

## 📈 **Results**
| Model              | Accuracy (%) |
|--------------------|--------------|
| Random Forest      | 83.24        |
| Gradient Boosting  | 81.01        |
| XGBoost            | 82.68        |
| LightGBM           | 83.80        |
| **Ensemble Model** | **84.94**    |

---

## 💡 **Insights**
- **Sex**: Females had a higher survival rate.
- **Pclass**: Higher classes (1st class) had better survival odds.
- **Family Size**: Passengers who were not alone had a higher survival rate.

---

## 📂 **File Structure**
```
titanic_project/
│-- README.md
│-- titanic.ipynb
│-- train.csv
│-- test.csv
```

---

## 🤝 **Acknowledgements**
- Kaggle for providing the Titanic dataset: [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic)

---

## 🔗 **References**
- Official Kaggle Titanic competition documentation.
- scikit-learn, XGBoost, and LightGBM documentation.

---

✨ **Happy Learning!** 🚀
