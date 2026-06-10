# ToxiGuard 🛡️
### Hate Speech and Toxic Comment Detection
**CCS3356 – Natural Language Processing | Sri Lanka Technology Campus**

---

## Group Members
| Member | Student ID | Branch | Models |
|--------|-----------|--------|--------|
| Member 1 | MEMBER1_ID | feature/MEMBER1_ID-model | Logistic Regression + CNN |
| Member 2 | MEMBER2_ID | feature/MEMBER2_ID-model | Random Forest + LSTM |
| Member 3 | MEMBER3_ID | feature/MEMBER3_ID-model | XGBoost + GRU |

---

## Problem Statement
ToxiGuard is an NLP-based system that detects hate speech and toxic comments
in online text. It classifies input into three categories:
- 0 — Hate Speech
- 1 — Offensive Language
- 2 — Neither

---

## Dataset
- **Name:** Hate Speech and Offensive Language Dataset
- **Source:** HuggingFace — `tdavidson/hate_speech_offensive`
- **Size:** 24,783 tweets
- **Classes:** Hate Speech / Offensive Language / Neither

### To download the dataset:
```python
from datasets import load_dataset
dataset = load_dataset("tdavidson/hate_speech_offensive")
df = dataset['train'].to_pandas()
df.to_csv("data/raw/hate_speech_offensive.csv", index=False)
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
| Member 1 | Logistic Regression | CNN | TF-IDF |
| Member 2 | Random Forest | LSTM | Bag of Words |
| Member 3 | XGBoost | GRU | TF-IDF + Bigrams |

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