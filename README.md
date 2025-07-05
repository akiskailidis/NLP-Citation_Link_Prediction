# NLP-Citation_Link_Prediction

Build a model to predict whether a paper cites another paper.

## Overview

In this project, we tackle the **link prediction** problem within academic citation networks. Given a dataset of research papers including their abstracts, authors, and citation information, the objective is to predict whether a citation (link) exists between two papers.

This problem is treated as a **binary classification** task, where each pair of papers is represented by a set of features, and the goal is to classify whether a citation link exists between them.

## Problem Description

Link prediction is the task of predicting the existence of a connection between two entities in a graph. In the context of academic citations, this means predicting whether one research paper cites another.

This task has applications in:
- Academic recommendation systems
- Bibliometrics
- Social networks (e.g., predicting friendships)
- Biology (e.g., predicting protein-protein or gene interactions)

In this challenge, you're provided with:
- A citation graph
- Abstracts of the papers
- List of authors for each paper
- Known citation links

## Approach

The pipeline for solving the problem involves:

1. **Feature Extraction**:
   - **Textual similarity** between paper abstracts (e.g., cosine similarity of TF-IDF or embeddings)
   - **Author overlap** or relatedness
   - **Graph-based metrics**, such as:
     - Common neighbors
     - Jaccard coefficient
     - Shortest path in the citation graph

2. **Data Preparation**:
   - Construct positive samples from existing citation links.
   - Construct negative samples from unlinked pairs.

3. **Model Training**:
   - Use machine learning classifiers (e.g., Logistic Regression, Random Forests, or Graph Neural Networks) to distinguish between cited and non-cited paper pairs.

4. **Evaluation**:
   - Use standard classification metrics: Accuracy, Precision, Recall, F1 Score, AUC-ROC.

5. **Prediction**:
   - Predict potential (undiscovered or future) citation links between papers.

## Technologies

- Python
- NetworkX or PyTorch Geometric (for graph processing)
- Scikit-learn
- NLP libraries (e.g., NLTK, SpaCy, HuggingFace Transformers)




