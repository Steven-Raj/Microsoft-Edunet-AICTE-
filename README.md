# Microsoft-Edunet-AICTE

# 🃏 Poker Hand Prediction using MLPClassifier

This project uses a Multi-Layer Perceptron (MLP) to classify different types of poker hands based on card suits and ranks.

## 📁 Dataset

- **Source**: [UCI Machine Learning Repository – Poker Hand Dataset](https://archive.ics.uci.edu/ml/datasets/Poker+Hand)
- Each hand has:
  - **5 cards** → Each card has a **suit (1–4)** and **rank (1–13)**
  - **10 features total** (5 cards × 2 attributes)
  - **Target label**: Poker hand type (0–9)

### 🎯 Hand Labels

| Label | Hand Type          |
|-------|--------------------|
| 0     | Zilch (Nothing)    |
| 1     | One Pair           |
| 2     | Two Pair           |
| 3     | Three of a Kind    |
| 4     | Straight           |
| 5     | Flush              |
| 6     | Full House         |
| 7     | Four of a Kind     |
| 8     | Straight Flush     |
| 9     | Royal Flush        |

> For better class balance, hands `>= 5` are grouped into a single class: `flush_or_better`.

---

## 🧠 Model

We use `MLPClassifier` from `scikit-learn`:

```python
MLPClassifier(
    solver='adam',
    alpha=0.05,
    hidden_layer_sizes=(50, 100, 50),
    learning_rate='adaptive',
    activation='tanh'
)
```


## 📊 Exploratory Data Analysis

Checked class distribution with Yellowbrick

Addressed class imbalance by merging underrepresented classes into one


## 🧪 Evaluation
Train Accuracy: ~77.6%

Test Accuracy: ~77.4%

Metrics Used:
Accuracy

Precision, Recall, F1-Score

ROC Curve

Classification Report

Class Prediction Error


## 📉 Visualizations
Visualized using Yellowbrick:

Class Balance

ROC Curve

Classification Report

Class Prediction Error

## 🧰 Tech Stack
Python

Pandas

Scikit-learn

Yellowbrick

Matplotlib


## 🔧 Install Requirements

pip install pandas scikit-learn yellowbrick matplotlib

##🚀 How to Run
Clone this repository

Install required packages

Open and run the Jupyter notebook:

jupyter notebook poker_hand_classifier.ipynb


## 📌 Future Enhancements
Apply ensemble models (RandomForest, XGBoost)

Improve class balance using SMOTE or oversampling

Deploy model using Streamlit or Flask for live predictions


## 🙏 Acknowledgments
Dataset: UCI Poker Hand Dataset

Visualizations: Yellowbrick

yaml


---

### ✅ Instructions to Use

1. Copy the content above into a file named `README.md`.
2. Place it in the root of your GitHub repository.
3. Commit and push the changes.

Let me know if you'd like a download link or if you want to add badges, author credits, or license deta
