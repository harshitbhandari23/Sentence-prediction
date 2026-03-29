# N-Gram Language Model (Text Prediction & Auto Text Generator)

## 📌 Project Overview

This project builds a **custom N-Gram Language Model** from scratch using **Python**.
It reads a large text corpus, creates **word sequences**, calculates **probability distributions**, and predicts the **next word**.

The project also supports **auto text generation** using learned probabilities.

---

## 🚀 Features

* Text preprocessing using Regex
* Custom N-Gram generation
* Probability distribution creation
* Next-word prediction
* Auto text generation
* No external NLP libraries required

---

## 🧠 How It Works

### Step 1 — Load Corpus

The model reads a large text file:

```python
with open('big.txt','r') as fd:
  lines=fd.readlines()
```

---

### Step 2 — Text Cleaning

* Convert to lowercase
* Remove punctuation
* Extract words using regex

```python
a=re.findall(r'\w+',sent.lower())
```

---

### Step 3 — Create N-Gram Pairs

The model creates word sequences:

| Type    | Example        |
| ------- | -------------- |
| Unigram | this           |
| Bigram  | this is        |
| Trigram | this is good   |
| 4-gram  | this is a good |

Custom function:

```python
def get_pairs(words,n):
```

---

### Step 4 — Probability Distribution

Using word frequency:

```python
from collections import Counter
```

Creates:

| Input     | Frequency | Output    |
| --------- | --------- | --------- |
| this is a | 20        | beautiful |
| this is a | 15        | good      |

---

### Step 5 — DataFrame Creation

```python
df=pd.DataFrame(prob,columns=["in",'freq','out'])
```

Example:

| in        | freq | out       |
| --------- | ---- | --------- |
| this is a | 20   | beautiful |

---

## 🔮 Next Word Prediction

Example:

```python
predict("this is a beautiful")
```

Output:

```text
day
place
city
```

---

## 🤖 Auto Text Generation

The model can generate full sentences:

```python
inp="of the united states"
```

Generated Output:

```text
of the united states of america is one of the largest...
```

This is done using iterative prediction:

```python
for i in range(50):
```

---

## 📊 Project Structure

```
project/
│
├── big.txt
├── ngram_model.py
├── README.md
└── requirements.txt
```

---

## 🛠️ Technologies Used

* Python
* Pandas
* Regex
* Collections
* Google Colab

---

## 📈 Applications

* Text Autocomplete
* Chatbot Generation
* Language Modeling
* Email Writing Assistant
* Smart Keyboard Prediction

---

## 🎯 Future Improvements

* Add smoothing techniques
* Use larger datasets
* Add UI using Streamlit
* Deploy as API

---

## 🧑‍💻 Author

Harshit Bhandari
Aspiring Data Analytics & NLP Engineer

---

## ⭐ Example Output

Input:

```
this is a beautiful
```

Output:

```
day place city country
```

---

## 📌 Conclusion

This project demonstrates **fundamental NLP concepts** including:

* Tokenization
* N-gram Modeling
* Probability Distribution
* Text Generation

A great beginner-to-intermediate NLP project.
