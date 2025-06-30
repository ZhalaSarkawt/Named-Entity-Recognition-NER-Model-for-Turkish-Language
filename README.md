# Named-Entity-Recognition-NER-Model-for-Turkish-Language
# 🧠 Named Entity Recognition (NER) Project

**Course:** YMT5250 - Natural Language Processing  
**Language:** Turkish  
**Library:** spaCy  

---

## 📁 Dataset

The dataset is in **CoNLL format**, containing manually annotated Turkish sentences.  
**Entity types include:**
- `PERSON`
- `CITY`
- `DATE`
- `AGE`
- `ORG`
- `PROFESSION`
- `EMAIL`
- *(and others like ZIP, FAX, URL, etc.)*

---

## ⚙️ Model Training

- Framework: **spaCy**
- Base Model: `spacy.blank("tr")` (Turkish)
- **Data Preprocessing:** Converted CoNLL data using offset spans for spaCy compatibility
- **Training Setup:**
  - 10 iterations
  - Mini-batch loop
- **Training Loss:**  
  Initial: `575` → Final: `116`

---

## 📈 Evaluation

- **Overall Accuracy:** `76.6%`
- **Best Performing Entities:**
  - `PERSON` (F1-score = **1.00**)
  - `CITY`
  - `PROFESSION`
- **Low Performing Entities:**
  - `ZIP`, `FAX`, `URL` (Likely due to limited examples)

---

## 🧪 Sample Predictions

**Example 1:**  
_Text:_  
`Prof. Fatma Özkan Antalya'da Cumhuriyet Bulvarı'nda...`  
_Predicted Entities:_  
- `Fatma Özkan` → `PERSON`  
- `Antalya` → `CITY`

---

## 📊 Classification Report

*(See image below)*  
![Classification Report](./path/to/classification_report.png)
