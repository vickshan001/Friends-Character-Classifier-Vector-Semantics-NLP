# 📚 Friends Character Classifier – Vector Semantics NLP Project (ECS763P 2024)

The aim is to classify which Friends character said a line of dialogue using vector space semantics and information retrieval techniques.

---

## 🎯 Objective

Build document representations for each Friends character using their lines from the TV show. Apply vector space semantics to identify speakers of unseen lines by comparing similarity between documents.

---

## 🔍 Key Features

### 🧹 Preprocessing
- Lowercasing, tokenization, stopword removal
- Stemming and lemmatization (POS-aware)
- Whitespace trimming

### 📊 Feature Extraction
- Unigrams & bigrams with `CountVectorizer`
- TF-IDF weighting with `TfidfVectorizer`
- POS tag frequency vectors
- Sentiment scores from VADER (NLTK)

### 🎭 Context-Aware Representation
- Character documents include scene-specific co-dialogue
- Scene and episode filtering ensures relevance
- Max line caps for balance (`max_lines=300` train, `30` val/test)

### 🧪 Evaluation
- Similarity-based document ranking using cosine similarity
- `compute_IR_evaluation_scores()` to measure:
  - 📈 Mean Rank
  - ✅ Accuracy

### 🔁 Grid Search
- Explored combinations of:
  - Preprocessing parameters
  - Feature inclusion (TF-IDF, POS, sentiment)
  - Context expansion

---

## 📈 Results

| Metric     | Validation Set | Test Set |
|------------|----------------|----------|
| Mean Rank  | **1.7**        | 1.7      |
| Accuracy   | **60%**        | 60%      |

**Top similarity:** Chandler ↔ Joey (0.924)  
**Least similarity:** Ross ↔ Aggregated group (0.863)

---

## 📂 Files Included

- `NLP_Assignment_2_distributional_semantics.ipynb` – Main notebook implementation  
- `Report - CW2 - VICKSHAN.pdf` – Final report write-up  

---

## 🏫 Coursework Info
- 📅 Year: 2023/24  
- 🏫 University: Queen Mary University of London  
- 👨‍💻 Author: Vickshan Vicknakumaran

---

## 🚀 How to Run

1. Open `NLP_Assignment_2_distributional_semantics.ipynb` in Jupyter Notebook  
2. Required Libraries:
   - `nltk`, `sklearn`, `pandas`, `matplotlib`, `seaborn`
3. Run all cells from top to bottom
4. Outputs: Similarity matrix heatmaps, rank/accuracy scores

---

## 📜 License

For academic and research use only.
