# `emotion-classifier`
A simple classification model that tries to answer the following question: What emotion (anger, fear, joy, love, sadness, surprise) does a message (sentence) display?

## Motivation
1. As an ML platform engineer, [Jay](https://www.linkedin.com/in/shilongjaycui/) wants to be able to empathize with his customers (data scientists) by becoming a data scientist himself.
2. Jay wants to answer data science questions related to mental health.

## Workflow
### Step 1: Get data.
- Hugging Face `dair-ai/emotion` dataset, which can be found [here](https://huggingface.co/datasets/dair-ai/emotion)

### Step 2: Featurize the data.
- scikit-learn's [TF-IDF](https://en.wikipedia.org/wiki/Tf%E2%80%93idf) vectorizer (`sklearn.feature_extraction.text.TfidfVectorizer`), which can be found [here](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html#sklearn.feature_extraction.text.TfidfVectorizer)

### Step 3: Train a model.
- sciklit-learn's random forest classifier (`sklearn.ensemble.RandomForestClassifier`), which can be found [here](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html#sklearn-ensemble-randomforestclassifier)

### Step 4: Evaluate the model.
- accuracy score
- classification report
- precision-recall curves
- confusion matrix
## Installation
1. Clone this repo on your local machine:
   ```bash
   $ git clone git@github.com:shilongjaycui/emotion-classifier.git
   ```
2. Navigate into the cloned repo:
   ```bash
   $ cd emotion-classifier
   ```
3. Create a virtual environment and activate it:
   ```bash
   $ python -m venv venv
   $ source venv/bin/activate
   ```
4. Install the dependencies, which are listed in Makefile:
   ```bash
   $ make install
   ```
5. Run the cells in the Jupyter Notebook (`emotion_classifier.ipynb`).
