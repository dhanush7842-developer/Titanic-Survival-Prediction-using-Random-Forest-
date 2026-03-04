# 🚢 Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using a **Random Forest** classifier.

## 📁 Project Structure

```
Titanic Survival Prediction/
├── Titanic Dataset.csv     # Raw dataset
├── Random Forest.ipynb     # Main notebook
└── README.md
```

## 📊 Dataset

The dataset contains information about Titanic passengers with the following key features:

| Feature | Description |
|---|---|
| `pclass` | Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| `sex` | Gender of the passenger |
| `age` | Age of the passenger |
| `sibsp` | Number of siblings/spouses aboard |
| `parch` | Number of parents/children aboard |
| `fare` | Ticket fare |
| `embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| `survived` | Survival (0 = No, 1 = Yes) — **Target Variable** |

## 🔧 Feature Engineering

- **FamilySize**: Derived as `sibsp + parch + 1` to capture the total number of family members aboard.
- **Sex encoding**: Converted to numeric values.
- **Embarked encoding**: One-hot encoded into `embarked_Q` and `embarked_S`.
- **Missing values**: Handled before model training.

## 🤖 Model — Random Forest

- **Algorithm**: Random Forest Classifier (ensemble of decision trees)
- **Features used**: `pclass`, `sex`, `age`, `fare`, `FamilySize`, `embarked_Q`, `embarked_S`
- **Train/Test split**: 80/20 with `random_state=42`

## 📈 Exploratory Data Analysis

The notebook includes visualizations such as:
- Survival count distribution
- Survival rate by passenger class
- Age distribution of passengers

## 🛠️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 🚀 Getting Started

1. Clone the repository
2. Install dependencies
3. Open the notebook in Jupyter and run all cells

```bash
jupyter notebook "Random Forest.ipynb"
```

## 📌 Key Insights

- **Passenger class** had a significant impact on survival rates
- **Gender** was one of the strongest predictors (women had higher survival rates)
- **Family size** and **age** also influenced survival outcomes
