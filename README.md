Co-occurrence Word Embeddings

This project provides a Python implementation for creating and visualizing count-based word embeddings from a text corpus. The script constructs a co-occurrence matrix, performs dimensionality reduction using Singular Value Decomposition (SVD), and plots the resulting 2D word vectors to reveal semantic relationships.

Description

Word embeddings are a fundamental concept in Natural Language Processing (NLP) where words are represented as dense numerical vectors. This implementation demonstrates a classic technique for generating these vectors based on word co-occurrence statistics. Words that appear in similar contexts will have similar vector representations.

The core logic follows these steps:

    1. Tokenize a sample text corpus.

    2. Build a co-occurrence matrix, counting how often words appear within a defined context window of each other.

    3. Apply TruncatedSVD to reduce the dimensionality of the sparse matrix into dense, low-dimensional embeddings.

    4. Visualize the final 2D embeddings on a scatter plot.

Features

    1. Distinct Word Extraction: Identifies all unique words (word types) in the corpus.

    2. Co-occurrence Matrix Construction: Builds a matrix based on a user-defined context window size.

    3. Dimensionality Reduction: Uses TruncatedSVD from scikit-learn to create dense vector embeddings.

    4. 2D Visualization: Plots the word vectors using matplotlib to visually inspect semantic similarities.

Adjust Parameters:

    window_size: Change this in the build_co_occurrence_matrix function call to control the context window. A larger window captures broader context, while a smaller one captures more syntactic relationships.

    k: Modify the dimension k in the reduce_dimensionality function call to change the final embedding size. For plotting, k must be 2.