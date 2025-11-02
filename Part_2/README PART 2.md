# **README — IRWA Project Part 2**

## **Overview**

This project is Part 2 of the IRWA assignment.  
 It builds an inverted index, performs TF–IDF ranking, and evaluates the search system using standard information retrieval metrics.  
 It also creates a manual ground truth based on conjunctive (AND) queries.

The notebook runs fully in **Google Colab**.

## **How to Run**

* Open the notebook in Google Colab.

* Run the first cell to install the required libraries (pandas, numpy, nltk, scikit-learn, matplotlib, seaborn).

* Upload the file **`fashion_products_clean.csv`** when prompted.

* The notebook will automatically load the data, build the inverted index, and compute TF–IDF vectors.

* Run the following cells in order — the notebook is designed to execute from top to bottom without changes.

* Later, upload **`validation_labels.csv`** when requested for the evaluation section.


  ## **Part 1 — Indexing**

* Builds an **inverted index** that maps each term to the documents containing it.

* Uses **conjunctive (AND) queries**, meaning only documents containing all query terms are retrieved.

* Creates a **TF–IDF representation** of all documents for ranking.

* Allows search and ranking using **cosine similarity**.

* Includes example queries such as:

  * “women blue cotton tshirt”

  * “men black jeans slim fit”

  * “women red dress long sleeve”


  ## **Part 2 — Evaluation**

* Implements standard information retrieval metrics:  
   Precision@K, Recall@K, F1@K, Average Precision, MAP, Reciprocal Rank, and NDCG.

* Evaluates two predefined queries using the provided **validation\_labels.csv** file:

  1. women full sleeve sweatshirt cotton

  2. men slim jeans blue

* Displays numeric results only, rounded to three decimals (analysis is done in the report).


  ## **Expert-Labeled Evaluation**

* Builds a **manual validation file** where documents are relevant if they satisfy the AND condition for the query.

* Evaluates five additional custom queries using this manual ground truth.

* Outputs all metric values numerically and includes optional debug visualizations of the top-ranked results.


  ## **Inputs and Outputs**

* **Inputs:**

  * `fashion_products_clean.csv` (dataset)

  * `validation_labels.csv` (provided relevance labels)

* **Output:**

  * `manual_validation_labels.csv` (automatically created)


  ## **Notes**

* The notebook produces numeric metric outputs only.

* All comments, analysis, and discussion should be written in the accompanying **report**.

* Runs entirely in Google Colab once the required files are uploaded.  
