# RMS-Titanic-Survival-Prediction

### Kaggle Competition Link:
https://www.kaggle.com/competitions/titanic

### Task:
Classification on Tabular Dataset of Titanic survivors.

### Dataset:

- **`train.csv`** – Contains passenger features along with survival labels.
- **`test.csv`** – Contains passenger features without survival labels.
- **`gender_submission.csv`** – Provides baseline predictions for the test set (used mainly for benchmarking).

#### Target Variable
- **`Survived`** (binary)
  - `1` → Passenger survived  
  - `0` → Passenger did not survive  



---

#### Feature Description

| Feature Name | Description |
|-------------|-------------|
| `PassengerId` | Unique identifier for each passenger |
| `Pclass` | Passenger class (1 = First, 2 = Second, 3 = Third) |
| `Name` | Passenger’s full name |
| `Sex` | Gender of the passenger |
| `Age` | Age in years (contains missing values) |
| `SibSp` | Number of siblings or spouses aboard |
| `Parch` | Number of parents or children aboard |
| `Ticket` | Ticket number |
| `Fare` | Passenger fare |
| `Cabin` | Cabin number (high proportion of missing values) |
| `Embarked` | Port of embarkation (`C` = Cherbourg, `Q` = Queenstown, `S` = Southampton) |

---

#### Dataset Characteristics

- **Problem Type:** Binary Classification  
- **Data Type:** Tabular / Structured  
- **Training Samples:** ~890  
- **Test Samples:** ~418  
- **Class Distribution:** Moderately imbalanced (more non-survivors than survivors)

---

#### Data Quality & Challenges

#### Missing Values
- `Age` contains missing entries.
- `Cabin` has a large proportion of missing values.
- `Embarked` contains a small number of missing entries.

#### Categorical Features
- `Sex`, `Embarked`, and `Ticket` require encoding.
- `Name` may be used for feature extraction (e.g., title parsing).

#### Feature Engineering Opportunities
- Family size: `SibSp + Parch`
- Title extraction from `Name`
- Fare normalization or binning
- Age imputation strategies

---

#### Evaluation Protocol

- Models are trained using **`train.csv`**
- Predictions are generated for **`test.csv`**
- Model performance may be evaluated using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - ROC-AUC

---

#### Intended Use

This dataset is suitable for:
- Learning supervised ML workflows
- Feature engineering experiments
- Model benchmarking and comparison
- Demonstrating end-to-end ML pipelines

---
#### Dataset provided by Kaggle.

### Model Used: Radom Forrest