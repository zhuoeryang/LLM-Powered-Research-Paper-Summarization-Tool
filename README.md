# LLM-Powered Research Paper Summarization Tool

## Overview

This project is a proof-of-concept (POC) for an LLM-based tool designed to extract and summarize key insights from academic research papers in PDF format. It leverages Langchain for document processing, OpenAI models for natural language understanding, and Streamlit for a simple user interface.

## Features

- Upload and load research papers in PDF format.
- Split long documents into manageable chunks using Langchain's `RecursiveCharacterTextSplitter`.
- Embed the text using `OpenAIEmbeddings` and store them in a vector database (Chroma).
- Query the document using a language model (`gpt-4o-mini`) to generate summaries or answer questions about the content.
- Provide evaluation capabilities using Langchain's evaluation tools.
- A user-friendly interface built with Streamlit for easy interaction.

## Tech Stack

- **Langchain**: For document loading, splitting, embedding, and LLM pipelines.
- **OpenAI GPT-4o-mini**: As the backend language model for summarization and Q&A.
- **Chroma**: A vector database for storing and querying embeddings.
- **Streamlit**: Used for building an interactive front-end application.
- **Python**: The core programming language used for this POC.
- **.env**: Used to securely manage API keys with `dotenv`.

## How it Works

1. **Document Loading**: The user uploads a PDF file which is loaded using `PyPDFLoader`.
2. **Text Splitting**: The PDF is split into smaller chunks for easier processing.
3. **Embedding**: Each chunk is converted into a vector using OpenAI’s embedding model.
4. **Vector Store**: These embeddings are stored in Chroma for efficient retrieval.
5. **Querying/Summarization**: The user can input questions or prompts, and the language model generates responses based on retrieved document chunks.
6. **Evaluation**: (Optional) Some tools are integrated for evaluating the model’s performance.

## Setup Instructions

1. Clone the repository.
2. Create a `.env` file with your OpenAI API key
3. Install the dependencies:
4. Run the Streamlit app

## Future Improvements

- Enhance the UI/UX for better usability.
- Support for multiple document formats.
- Incorporate fine-tuned LLMs or RAG pipelines.
- Add export functionality for summaries.

## References

This project was inspired and guided by the work of Extracting Structured Data From PDFs by Thu vu
- Langchain documentation: https://docs.langchain.com/
- Streamlit documentation: https://docs.streamlit.io/
- OpenAI API documentation: https://platform.openai.com/docs