# 🚫 SpamShield: Real-Time Email & SMS Spam Classifier

SpamShield is a lightweight Streamlit-based web application that detects whether a given text message (SMS or Email) is spam or not. It uses natural language processing (NLP) and machine learning to process, vectorize, and classify the input text.

---

## ✨ Features

- 📥 Classifies user input as **Spam** or **Not Spam**
- 🧠 Uses a trained machine learning model with TF-IDF vectorization
- 🔤 Includes text preprocessing like:
  - Lowercasing
  - Stopword removal
  - Punctuation removal
  - Tokenization
  - Stemming
- 🌐 Interactive web interface powered by Streamlit

---

## 📂 Dataset

Model is trained on a public SMS Spam Collection dataset (`spam.csv`), which contains labeled SMS messages as spam or ham.

Dataset includes:
- `label`: spam/ham
- `message`: the actual SMS content

---

## 🛠️ Tech Stack

| Tool/Library        | Purpose                        |
|---------------------|--------------------------------|
| Python              | Core Programming Language      |
| Streamlit           | Web App Interface              |
| NLTK                | NLP Preprocessing              |
| scikit-learn        | TF-IDF Vectorizer & ML Model   |
| Pickle              | Model and Vectorizer Storage   |

---

## 🧪 Methodology

1. **Text Preprocessing**:
   - Lowercasing
   - Removing stopwords and punctuation
   - Tokenization and stemming using NLTK

2. **Feature Extraction**:
   - TF-IDF Vectorization of cleaned text

3. **Classification**:
   - Trained classifier (e.g., Multinomial Naive Bayes or Logistic Regression)
   - Prediction based on vectorized input

---

## 🖥️ Usage

### 🔧 Installation

1. Clone the repo:
```bash
git clone https://github.com/yourusername/spamshield.git
cd spamshield
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Make sure your model files exist:

* `model.pkl`: Trained spam classifier
* `vectorizer.pkl`: Fitted TF-IDF vectorizer

4. Run the app:

```bash
streamlit run app.py
```

---

## 📦 requirements.txt

```txt
streamlit>=1.20.0
nltk>=3.8.0
scikit-learn>=1.1.0
```

Make sure to download NLTK resources before running:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

---

## 🖼️ Sample Output

Input:

```
Congratulations! You've won a free iPhone. Claim now.
```

Output:

```
Spam
```

---

## 🧠 Possible Enhancements

* Support multilingual spam detection
* Visualize model confidence and probabilities
* Train with updated datasets or deep learning models

---


## 📜 License

This project is open-source and available under the MIT License.

