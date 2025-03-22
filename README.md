#Enhancing Search Engine Relevance for Video Subtitles (Cloning Shazam)

**Overview**

This project focuses on improving the relevance of search results for video subtitles using Natural Language Processing (NLP) and machine learning techniques. By leveraging both keyword-based and semantic search strategies, the system enhances the accessibility of video content, making it easier for users to find relevant subtitles based on their queries.

**Features**

Keyword-Based Search: Uses TF-IDF/BOW models to match exact words in subtitles.

Semantic Search: Employs BERT-based embeddings for understanding contextual meaning.

Efficient Data Processing: Cleans, preprocesses, and chunks subtitles to optimize search accuracy.

Audio-Based Query: Accepts user queries in audio format, transcribes them, and retrieves matching subtitles.

Fast Retrieval: Utilizes cosine similarity and FAISS/ChromaDB for quick document retrieval.

**Dataset**

The dataset required for this project is available on Google Drive:https://drive.google.com/drive/folders/1VHE1c76nNbcbmKRt4qgZJSzx2nCY48HB?usp=sharing

**Usage**

Step 1: Ingesting Documents

Load subtitle data from the database.

Apply preprocessing (cleaning timestamps, removing noise, etc.).

Generate embeddings using TF-IDF or BERT-based SentenceTransformers.

Use document chunking with overlapping windows to preserve context.

Store embeddings in a ChromaDB database.

Step 2: Retrieving Documents

Accept a 2-minute audio query from a TV series or movie.

Transcribe the query into text.

Create embeddings for the transcribed query.

Compute cosine similarity scores to find the most relevant subtitle segments.

Return top-matching subtitle documents.

**Technologies Used**

Python

NLP Libraries: NLTK, spaCy

Machine Learning: SentenceTransformers, BERT

Vector Databases: FAISS, ChromaDB

Audio Processing: SpeechRecognition

Data Processing: Pandas, NumPy
