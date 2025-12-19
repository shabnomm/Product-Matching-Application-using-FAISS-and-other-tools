Product Matching Application using FAISS

This repository contains a semantic product matching system built using Sentence Transformers, FAISS, and Streamlit. The application retrieves the most similar products from a large catalog based on semantic similarity and provides an interactive dashboard for exploration and evaluation.

📌 Project Overview

Traditional keyword-based product matching often fails due to inconsistent naming and incomplete metadata. This project addresses that limitation by using embedding-based semantic similarity combined with efficient vector search (FAISS).

Key features include:

Semantic product matching using embeddings

Fast similarity search with FAISS

Optional hybrid re-ranking (semantic + lexical)

Performance evaluation using standard IR metrics

Interactive Streamlit dashboard

📂 Dataset

Total products: 4,566

Domains: Fashion and lifestyle products

Key fields:

Product ID

Product Name

Brand Name

Category

Description

Size

Price and Discount

Note: Ground-truth matching pairs were not available. Category-based relevance was used for evaluation.

⚙️ Methodology

Text Construction
Product attributes are concatenated into a single textual representation.

Embedding Generation
Sentence-Transformers (all-MiniLM-L6-v2) converts product text into dense vectors.

Similarity Search
FAISS IndexFlatIP is used with cosine similarity for fast retrieval.

Hybrid Re-Ranking (Optional)
Combines semantic similarity with fuzzy keyword matching for improved practical accuracy.

Evaluation
Performance is measured using:

Precision@K

Recall@K

MAP@K

MRR@K

nDCG@K

📊 Performance Summary

The system achieves:

>99% Precision@K

Strong ranking quality (high MAP and MRR)

Stable performance across different K values

Detailed results are provided in the report and evaluation tables.

🖥️ Interactive Dashboard

A Streamlit dashboard is provided to:

Search by Product ID or free-text query

View top-K matched products

Apply category, brand, and price filters

Compare products side-by-side

Download results as CSV

View evaluation metrics and dataset statistics

Dashboard Link:
👉 (https://pseudonymously-matrilateral-jenee.ngrok-free.dev/)

📌 Use Cases

Semantic product search

Product recommendation systems

Catalog deduplication

Similar item retrieval

E-commerce analytics

📎 Notes

FAISS provides fast and scalable similarity search.

Hybrid re-ranking improves real-world matching when product names contain important keywords.

The system is designed to be extensible to larger datasets or different domains.

🏁 Conclusion

This project demonstrates that embedding-based semantic retrieval combined with FAISS is an effective and scalable solution for product matching. The high precision and strong ranking performance make the system suitable for real-world e-commerce applications.
