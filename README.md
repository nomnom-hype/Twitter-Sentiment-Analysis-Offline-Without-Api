# Twitter-Sentiment-Analysis-Offline-Without-Api
Mini Autonomous Policy Intelligence Agent

Offline X (Twitter) Policy Analysis using Sentiment140

Project Overview

This project implements a lightweight AI-driven Policy Intelligence Agent designed to analyze policy-related discourse from Twitter (X) using the Sentiment140 dataset as an offline proxy. The system demonstrates data filtering, sentiment analysis (Positive/Negative/Neutral), topic modeling, semantic embeddings, vector database retrieval (FAISS), agent-based orchestration, and executive insight generation.

Objective

Build a modular NLP intelligence system that filters tweets using a policy keyword, performs sentiment classification, extracts top 3 topics, enables semantic retrieval, routes queries via an agent layer, and generates an executive-level intelligence report.

Dataset

Source: Sentiment140 (Kaggle)  
Size: 1.6M tweets  
Subset Used: Tweets containing the keyword 'bank' for financial policy relevance.

System Architecture

1.  Data Loading & Keyword Filtering ('bank')  
    2\. Text Cleaning (regex-based preprocessing)  
    3\. Sentiment Model (TF-IDF + Logistic Regression with Neutral threshold)  
    4\. Topic Modeling (LDA - 3 interpretable topics)  
    5\. Embeddings (all-MiniLM-L6-v2)  
    6\. FAISS Vector Database  
    7\. Agent Router  
    8\. Executive Report Generator

                             Sentiment140 Dataset

                                      │

                                      ▼

                          Keyword Filtering ("bank")

                                      │

                                      ▼

                                Text Cleaning

                                      │

├ 

Sentiment Model      ----------Topic Modeling             -----------Embeddings                       

(TF-IDF + LR)       ------------(LDA - 3 topics)             ------------(MiniLM)                        



└      ─────────────      ┴     ──────────────      ┴        ───────┬──────      ┘

                                                                    ▼

                                                              FAISS Vector DB

                                                                    │

                                                                    ▼

                                                              Agent Router

                                                                    │

                                                                    ▼

                                                        Executive Report Generator

Sentiment Analysis

Model: TF-IDF + Logistic Regression  
Neutral sentiment is derived using a probability threshold to capture model uncertainty.  
Outputs include Positive, Negative, Neutral distribution and overall confidence score.

Topic Modeling

Method: Latent Dirichlet Allocation (LDA)  
Extracts 3 key topics with top keywords and representative tweets for interpretability.

Embeddings & Vector Database

Embedding Model: all-MiniLM-L6-v2 (open-source, locally executed)  
Vector Database: FAISS (IndexFlatL2) for semantic retrieval.

Agent Layer

A lightweight rule-based router directs user queries to:  
\- Sentiment Summary Tool  
\- Topic Exploration Tool  
\- RAG-based Semantic Retrieval Tool

Executive Intelligence Report

Automatically generates:  
\- Sentiment distribution (Positive / Negative / Neutral)  
\- Top 3 topics with keywords  
\- Narrative summary  
\- Risk insight  
\- Confidence score

Compliance Statement

This project strictly adheres to assignment constraints:  
No paid APIs, no live Twitter scraping, no proprietary datasets, no SaaS tools, and no AutoML platforms. All models are open-source and executed locally.

Engineering Principles

Modular design, separation of concerns, interpretability, lightweight implementation, defensive programming, and reproducibility.
