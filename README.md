# QAsystem
Document Based Question Answering System
PDF to Text and Semantic Search

This Python script demonstrates how to convert a PDF file to text using the PDFMiner library and perform semantic search on the extracted text using the Sentence Transformers library. The script is divided into two main parts: PDF to Text Conversion and Semantic Search.
PDF to Text Conversion
Function: pdf_to_text

The pdf_to_text function converts a PDF file into plain text. It uses the PDFMiner library to extract text from the PDF. The function takes the path to the PDF file as input and returns the extracted text.
Semantic Search

The script performs semantic search on the extracted text using Sentence Transformers, a powerful library for text embeddings.
Tokenization

The extracted text is tokenized into paragraphs using the text_to_paragraphs function. Each paragraph is separated by two consecutive newline characters (\n\n).
Sentence Embeddings

The script uses the Sentence Transformers library to create sentence embeddings for each paragraph in the text. It uses the "all-mpnet-base-v1" model for this purpose. The embeddings are stored in the embeddings variable.
Semantic Search Queries

The script defines a list of semantic search queries, such as:

    "Who can appoint commissioned officer in the army?"
    "Who cannot enroll in the Indian Army?"
    "Who are subjected to this act?"
    "What is the punishment for escape from custody?"
    "Explain regular army?"

Semantic Search

For each query, the script finds the closest two sentences in the corpus (extracted text) based on cosine similarity. It calculates the cosine similarity between the query embedding and the embeddings of all the paragraphs in the corpus to find the most semantically similar sentences.
Running the Script

    PDF to Text Conversion: The script starts by converting the PDF file located at the specified path to plain text.

    Semantic Search: After extracting the text and creating sentence embeddings, the script performs semantic search for each query and displays the top two most similar sentences in the corpus for each query.

Dependencies

    PDFMiner: For PDF to text conversion.
    Sentence Transformers: For sentence embeddings and semantic search.

Note

This script is a basic example of PDF to text conversion and semantic search. You can customize it for your specific use case, such as searching for specific information within large documents.
