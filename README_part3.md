# IRWA Project – Part 3

Conjunctive ranking using TF-IDF, BM25, a custom score, and Word2Vec-style embeddings on the `fashion_products_clean.csv` dataset.

## Requirements

The notebook installs everything automatically:
- pandas
- numpy
- scikit-learn
- rank-bm25
- gensim

Recommended environment: Google Colab.

## How to Run

1. Open `IRWA_Project_Part_3.ipynb` in Google Colab.
2. Run the first cell and upload `fashion_products_clean.csv` when prompted.
3. Run all remaining cells in order (Runtime → Run all).

No code modifications are needed.

## What the Notebook Does

- Loads and inspects the cleaned dataset.
- Builds a unified text field and a token-based inverted index.
- Applies strict conjunctive filtering (AND semantics) to all queries.
- Implements four ranking functions:
  - search_tfidf (TF-IDF + cosine similarity)
  - search_bm25 (BM25 lexical ranking)
  - search_your_score (BM25 + rating + discount – stock penalty)
  - search_word2vec (GloVe embeddings + cosine similarity)
- Executes these methods on the project queries.
- Generates:
  - per-method result tables,
  - per-query comparison tables,
  - optional CSV exports for all rankings.

## Expected Behavior

- Queries with all terms present in the dataset return ranked results.
- Queries missing at least one term (after preprocessing) return zero candidates for all ranking functions.
- Comparison tables should be used in the Part 3 report.
