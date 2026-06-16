# ToxiGuard 🛡️
### Hate Speech and Toxic Comment Detection
**CCS3356 – Natural Language Processing | Sri Lanka Technology Campus**

---

## Group Members
| Member | Student ID | Branch | Models |
|--------|-----------|--------|--------|
| Dileepa Alwis | CIT-24-01-0325 | feature/MEMBER1_ID-model | Logistic Regression + CNN |
| Kalindu Himsara | CIT-24-01-0597 | feature/MEMBER2_ID-model | Random Forest + LSTM |
| Nisal Chathushka | CIT-24-01-0117 | feature/MEMBER3_ID-model | XGBoost + GRU |

---

## Problem Statement
ToxiGuard is an NLP-based system that detects hate speech and toxic comments
in online text. It classifies input into two categories:
- **0** — Not Toxic (Normal comment)
- **1** — Toxic (Hate Speech / Offensive Language)

---

## Dataset

| Field | Details |
|-------|---------|
| Name | Toxic Comment Classification |
| Source | Kaggle — `akashsuper2000/toxic-comment-classification` |
| Original Size | 119,518 comments |
| Balanced Size | 80,000 comments |
| Classes | 0 — Not Toxic / 1 — Toxic |

### To download the dataset:
```bash
# Install Kaggle API first
pip install kaggle

# Download dataset
kaggle datasets download -d akashsuper2000/toxic-comment-classification
```

```python
import pandas as pd

df = pd.read_csv("data/raw/train.csv")
print(df.shape)       # (119518, 8)
print(df.head())
df.to_csv("data/raw/toxic_comments.csv", index=False)
```


---

## Setup Instructions
```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/NLP_Group_XX.git
cd NLP_Group_XX

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate        # Mac/Linux
venv\Scripts\activate           # Windows

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download the dataset
python -c "
from datasets import load_dataset
ds = load_dataset('tdavidson/hate_speech_offensive')
ds['train'].to_pandas().to_csv('data/raw/hate_speech_offensive.csv', index=False)
"
```

---

## How to Run the App
```bash
cd src
python app.py
# Open http://127.0.0.1:5000 in your browser
```

---

## Model Summary
| Member | ML Model | DL Model | Feature Engineering |
|--------|----------|----------|-------------------|
| Dileepa Alwis | Logistic Regression | CNN | TF-IDF |
| Kalindu Himsara | Random Forest | LSTM | Bag of Words |
| Nisal Chathushka | XGBoost | GRU | TF-IDF + Bigrams |

---

## Results Summary
*(To be updated after model evaluation)*

| Model | Accuracy | F1-Score | ROC-AUC |
|-------|----------|----------|---------|
| Logistic Regression | - | - | - |
| Random Forest | - | - | - |
| XGBoost | - | - | - |
| CNN | - | - | - |
| LSTM | - | - | - |
| GRU | - | - | - |

---

## Project Structure
NLP_Group_XX/
├── data/               # Dataset files (not tracked by Git)
├── notebooks/          # Individual member notebooks
├── src/                # Flask app source code
├── models/             # Saved trained models
├── templates/          # HTML templates
├── static/             # CSS and JS files
├── reports/            # Final report
├── screenshots/        # App screenshots
├── videos/             # Demo videos
├── requirements.txt
└── README.md