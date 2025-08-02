
# 🧠 AI Writing Style Fingerprinter

> ⚠️ **Note:** This project was tested with a small, random dataset of ~30–40 examples, mostly for experimentation.  
Feel free to create your own dataset to train a more accurate and robust model.

---

## 📌 Overview

**AI Writing Style Fingerprinter** is a lightweight machine learning project designed to detect whether a paragraph was written by **ChatGPT**, **Claude**, or a **Human**, based purely on **shallow linguistic features**.

It uses:
- Part-of-speech ratios
- Sentence structure statistics
- Punctuation and stopword frequency

All without deep learning—only `spaCy`, `scikit-learn`, and some classic ML.

---

## 📂 Dataset Format

The dataset should be a CSV file named `dataset.csv` with the following structure:

```csv
text,label
"AI helps personalize education.",ChatGPT
"The cat sat on the mat.",Human
"By leveraging ML, performance improves.",Claude
````

---

## ⚙️ Features Extracted

* Average sentence length
* Punctuation count
* Stopword ratio
* Noun / Verb / Adjective ratios (POS-based)
* Number of sentences and tokens

---

## 🚀 Getting Started

### 1. Install dependencies

```bash
pip install pandas scikit-learn spacy matplotlib
python -m spacy download en_core_web_sm
```

### 2. Run the model

```bash
open  main.ipynb and run the code
```

This will:

* Load the dataset
* Extract linguistic features
* Train a `RandomForestClassifier`
* Print a classification report and confusion matrix
* Allow optional predictions on custom text

---

## 🧪 Example Usage

```python
predict("AI can enhance teaching by providing real-time feedback.")
# ➜ Prediction: ChatGPT
```

---

## 📈 Outputs

* Confusion matrix plot (`matplotlib`)
* Classification metrics: Precision, Recall, F1-score
* Feature importance bar chart

---

## 📌 Notes

* Designed for quick testing; feel free to expand dataset for better performance.
* You can integrate `Streamlit` to create a live interface if needed.

---

## 🧠 Author

**Pujan Neupane**
[GitHub](https://github.com/pujan-dev) • [Portfolio](https://neupanepujan.com.np)

