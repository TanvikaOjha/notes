# Embeddings
Embedding converts text into numbers in such a way that similar meanings end up close to each other in a mathematical space. This allows AI systems to search based on meaning and relationship between words rather than exact matches.

Technically, embeddings are vectors created by ML models for the purpose of capturing meaningful data about each object.

## What is a vector?
A vector is an array of numbers that define a point in a dimensional space. Each number indicates where the object is along a specified dimension. In ML, use of vectors makes it possible to search for similar objects. A vector searching algo simply has to find two vectors that are close together in a vector database. ML models tend to generate multi-dimensional complex vectors.

## How embeddings work?
Embedding is the process of creating vectors using deep learning. An embedding is the output of the process. Using embeddings, an algo can suggest a relevant TV show, find similar locations, or identify which words are likely to be used together or similar to each other, as in language models.

The creation of embedding is a hidden layer. It usually takes place before additional layers process the input.
Creating an embedding layer requires some manual effort at first. A programmer may feed the NN examples of to create an embedding, which dimensions to include, and so on. Eventually, the embedding layer can operate on it's own-although for better recommendation fine tuning should be done.

## How are embeddings used in LLMs
For LLMs, embedding is taken a step further.The context of each word becomes an embedding in addition to the word itself. Although this takes a lot of computatiional power, it saves time and compute power for future queries.


## Use Cases
1. Text Search-an embedding model will convert your query to numbers and retrieve documents with similar embeddings.
2. Recommend movies
3. Match images and caption
4. Group similar items