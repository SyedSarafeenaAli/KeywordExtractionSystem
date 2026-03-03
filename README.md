# NETWORK URL:-

http://127.0.0.1:5000

# THEORY:-

KEYWORD EXTRACTION:

Keyword Extraction is a Natural Language Processing (NLP) technique used to automatically identify the most important words or phrases in a document. These keywords summarize the core content and help in information retrieval, document indexing, topic identification, and search optimization.
Unlike text classification, keyword extraction does not assign a category label. Instead, it identifies significant terms based on statistical importance within the document.

TF-IDF (Term Frequency – Inverse Document Frequency):

TF-IDF is a statistical method used to measure how important a word is in a document relative to a corpus.
It consists of two components:

Term Frequency (TF): Measures how frequently a word appears in a document.

Inverse Document Frequency (IDF): Measures how rare a word is across all documents.

Formula:

TF-IDF = TF × IDF

Words that appear frequently in a document but rarely across the corpus receive higher TF-IDF scores, making them strong candidate keywords.

COUNT VECTORIZER:

CountVectorizer is a feature extraction technique that converts text into a matrix of token counts (Bag-of-Words model). It creates a vocabulary of all words in the corpus and represents each document as a vector of word frequencies.

TF-IDF TRANSFORMER:

TfidfTransformer converts the CountVectorizer output into a TF-IDF weighted representation, emphasizing informative words and reducing the impact of common words.

# PROBLEM STATEMENT:-

Large volumes of textual data are generated daily in research papers, articles, reports, and digital content. Manually identifying important terms from such documents is time-consuming and inefficient.

The problem addressed in this project is:

"To develop an automated NLP-based system capable of extracting the most relevant keywords from a given document using statistical text processing techniques."

# OBJECTIVES:-

The main objectives of this project are:

1. Text Preprocessing

a) Clean raw textual data

b) Remove noise (HTML tags, punctuation, special characters)

c) Remove stopwords

d) Perform tokenization

e) Apply lemmatization

2. Feature Engineering

a) Convert text into numerical format using CountVectorizer

b) Apply TF-IDF transformation for weighting terms

3. Keyword Extraction

a) Rank terms based on TF-IDF scores

b) Extract top-N keywords from a document

4. Deployment

a) Build a Flask-based web interface

b) Allow users to upload text documents

c) Display extracted keywords dynamically

# DATASET AND FEATURES:-

DATASET:

This project does not rely on a fixed public dataset during runtime. Instead, it uses a training corpus used to build:-

count_vectorizer.pkl

tfidf_transformer.pkl

feature_names.pkl

These serialized files are generated from a pre-trained corpus and loaded during application execution.

# PREPROCESSING STEPS:-

The preprocessing pipeline includes:

1. Lowercasing text

2. Removing HTML tags

3. Removing digits and special characters

4. Tokenization using NLTK

5. Stop-word removal

6. Removing words with less than 3 characters

7. Lemmatization using WordNetLemmatizer

# FEATURE REPRESENTATION:-

FEATURE TYPE                     DESCRIPTION                             	   TOOL USED

Token Frequency	    Basic Bag-of-Words word count representation	         CountVectorizer

TF-IDF Weighting	  Weighted importance of words within corpus	           TfidfTransformer

Ranked Keywords	    Top N highest scoring terms extracted per document	   Custom Ranking Logic
