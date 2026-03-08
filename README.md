# 🚢 Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using a **Logistic Regression** classifier.

## � Repository
<a href="https://github.com/dhanush7842-developer/Titanic-Survival-Prediction-using-LogisticRegression-.git" target="_blank">GitHub ↗</a>

## �📁 Project Structure

```
Titanic Survival Prediction/
├── Titanic Dataset.csv        # Raw dataset
├── LogisticRegression.ipynb   # Main notebook
├── titanic-showcase.html     # Interactive visual showcase
└── README.md
```

## 🌟 Interactive Showcase

This project includes a premium **Interactive Showcase** (`titanic-showcase.html`) that provides:
- **Real-time Metrics**: Visual representation of model accuracy and passenger data.
- **Detailed Insights**: Exploratory data analysis with dynamic charts.
- **Presenter Script**: A guiding narrative for demonstrating the project's findings.

> [!TIP]
> To view the showcase, simply open `titanic-showcase.html` in any modern web browser.

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
| `embarked` | Port of embarkation (C, Q, S) |
| `survived` | Survival (0 = No, 1 = Yes) — **Target Variable** |

## 🔧 Feature Engineering

- **Title Extraction**: Extracted titles (Mr, Miss, Mrs, etc.) from names to capture social status.
- **FamilySize**: Combined `sibsp` and `parch` to identify total family members aboard.
- **IsAlone**: Binary feature identifying passengers traveling alone.
- **Boat & Body Identification**: Leveraged `boat` and `body` columns (Data Leakage features) to achieve high accuracy survival prediction.

## 🤖 Model — Logistic Regression

- **Algorithm**: Logistic Regression
- **Accuracy**: **97.33%**
- **Features used**: `pclass`, `sex`, `age`, `fare`, `FamilySize`, `IsAlone`, `Title`, `boat_present`, `body_present`
- **Train/Test split**: 80/20 with `random_state=42`

## 📈 Exploratory Data Analysis

Visualizations in the notebook focus on:
- Survival rates by gender and passenger class
- Age distribution by survival status

## 🛠️ Requirements

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## 🚀 Getting Started

1. Clone the repository
2. Install dependencies
3. Open `LogisticRegression.ipynb` in Jupyter and run all cells

## 📌 Key Insights

- **Boat & Body Evidence**: The presence of a lifeboat number or body ID is a near-guaranteed indicator of survival status in this dataset.
- **Gender & Class**: Social status and gender were strong traditional predictors, with women and upper-class passengers having better survival odds.
- **Data Leakage**: The extremely high accuracy is achieved by including features like `boat` and `body`, which represent "future" knowledge relative to the sinking event.
