# Resume Screening System using Machine Learning & NLP

## 📌 Overview
This project presents an automated resume screening system using Machine Learning (ML) and Natural Language Processing (NLP). The system classifies candidates as **suitable (1)** or **not suitable (0)** based on resume data.

The project demonstrates:
- Text processing using TF-IDF
- Use of structured features (experience, degree, portfolio)
- Model comparison (Logistic Regression, Random Forest, SVM)
- Identification of dataset limitations (100% accuracy issue)

---

## 📊 Dataset
- Source: Kaggle Resume Screening Dataset
- Link: https://www.kaggle.com/datasets/kawsertalukder/resume-screening-dataset4500
- Size: 4500 samples
- Features:
  - Structured: years_experience, highest_degree, has_portfolio
  - Text: raw_text
  - Target: label (0/1)

⚠️ Note: Dataset is synthetic with strong patterns.

---

## ⚙️ Features Implemented
- Data preprocessing (cleaning, stopwords removal)
- TF-IDF vectorization (text features)
- Structured feature encoding
- Hybrid feature matrix (text + structured)
- Model training and evaluation
- Cross-validation
- Model saving and prediction system

---

## 🤖 Models Used
- Logistic Regression (baseline)
- Random Forest
- Support Vector Machine (SVM)

---

## 📈 Results Summary
| Model Type | Accuracy | Insight |
|------------|--------|--------|
| Text-only | 100% ❌ | Misleading due to dataset patterns |
| Structured | ~87% ✅ | Realistic performance |
| Hybrid | High | Influenced by text bias |

---

## 🚨 Key Insight 
Data quality is more important than model complexity.

---

## 🛠️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/resume-screening.git
cd resume-screening
```
## Install dependencies:
```bash
pip install -r requirements.txt
```
## Reproduction Steps:
1. Open in Google Colab or local environment

Upload dataset:
```bash
/content/ml_resume_dataset_4500.csv
```
2. Run preprocessing
- Clean text (lowercase, remove punctuation, stopwords)
- Remove leakage column (current_title)
- Encode structured features

3. Feature Engineering
- Apply TF-IDF (max_features=50)
- Combine with structured features

4. Train/Test Split
```bash
train_test_split(test_size=0.2, stratify=y)
```
5. Train Models
- Logistic Regression
- Random Forest
- SVM

6. Evaluate Models
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
-Cross-validation

7. Save Model
```bash
joblib.dump(model, 'resume_model.pkl')
```
8. Run Prediction
```bash
predict_candidate(years_experience, degree, has_portfolio)
```

# THANK YOU!!
