# NLP-Encoding-Embedding

A comprehensive repository demonstrating text encoding and embedding techniques in Python for natural language processing.

## Contents

- `main.py` — main script for running encoding workflows
- `pyproject.toml` — project configuration and dependencies
- `requirements.txt` — package dependencies for notebook and examples
- `One-Hot-Encoding/` — One-hot encoding examples
  - `OneHotEncoding.ipynb` — comprehensive one-hot encoding techniques
- `Encoding/` — Various text encoding methods
  - `BagOfWords.ipynb` — Bag of Words encoding implementation
  - `OneHotEncoding.ipynb` — One-hot encoding for categorical variables
  - `TF-IDF.ipynb` — TF-IDF (Term Frequency-Inverse Document Frequency) encoding

## Encoding Techniques

### 1. One-Hot Encoding
Converts categorical variables into binary vectors where only one position is 1 and others are 0.

**Use Cases:**
- Binary representation of categorical features
- Machine learning models that require numerical inputs
- Converting nominal variables (e.g., colors, categories)

**Advantages:**
- Simple and interpretable
- No ordinal relationship implied
- Works well with tree-based models

**Disadvantages:**
- Creates sparse matrices for high-cardinality features
- Curse of dimensionality with many categories

### 2. Bag of Words (BoW)
Represents text as an unordered collection of word frequencies.

**Use Cases:**
- Text classification
- Sentiment analysis
- Document similarity
- Simple baseline for NLP tasks

**How it Works:**
- Creates a vocabulary of unique words
- Counts word occurrences in each document
- Ignores word order and grammar

**Advantages:**
- Simple to understand and implement
- Fast to compute
- Good baseline for text analysis

**Disadvantages:**
- Loss of word order information
- Ignores semantic meaning
- May require stopword removal and preprocessing

### 3. TF-IDF (Term Frequency-Inverse Document Frequency)
Numerical statistic reflecting word importance in a document relative to a corpus.

**Formula:**
- TF = word frequency in document / total words in document
- IDF = log(total documents / documents containing word)
- TF-IDF = TF × IDF

**Use Cases:**
- Information retrieval
- Document ranking
- Feature extraction for text classification
- Search engine scoring

**Advantages:**
- Weights common and rare words appropriately
- Better semantic representation than raw BoW
- Reduces impact of frequently occurring words

**Disadvantages:**
- Still ignores word order
- Computationally more expensive than BoW
- May require preprocessing and tuning

## Setup

```bash
python -m pip install -r requirements.txt
```

If you use Python 3.11.15 and need a dedicated Jupyter kernel:

```bash
python -m ipykernel install --user --name python311 --display-name "Python 3.11.15"
```

## Running the notebooks

Open the notebooks in Jupyter or VS Code and run the cells interactively:

- `One-Hot-Encoding/OneHotEncoding.ipynb`
- `Encoding/TF-IDF.ipynb`

## Git

This repository is initialized with git and uses `origin` as the remote upstream. Commit changes and push using:

```bash
git add .
git commit -m "Your message"
git push -u origin main
```
