# Jasper's Legal-Assistant
Completed as my Capstone project for the 5 day intensive Google/Kaggle GenAI for Developers course in Q1 2025.

This is an AI-powered tool designed to assist legal professionals in Kenya with case summarization, legal research, and document drafting. This project is a capstone from Google and Kaggle's 5-day GenAI course for developers, leveraging advanced AI technologies to support Kenyan legal practice.

## Features

-   **Legal Research**: Search Kenyan case law and statutes using vector embeddings and Google Search integration.
-   **Case Summarization**: Generate brief or comprehensive summaries, extracting key facts, holdings, and citations.
-   **Document Generation**: Create formatted legal documents like petitions, memos, and affidavits based on user inputs.
-   **Interactive Interface**: Access all features through a Gradio-based web interface.

## Technologies Used

-   **Google's Gemini Pro**: Powers natural language generation and analysis.
-   **Vector Embeddings**: Custom SimpleVectorStore for semantic search of legal documents.
-   **LangChain**: Manages AI orchestration and document handling.
-   **LangGraph**: Enables agent-based workflows for complex tasks.
-   **RAG (Retrieval-Augmented Generation)**: Ensures grounded, context-aware responses.
-   **Gradio**: Provides an interactive UI for user interaction.

## Setup Instructions

Follow these steps to set up and run Jasper's Kenyan Legal Assistant locally:

1.  **Clone the Repository**
    
    bash
    
    CollapseWrapCopy
    
    `git clone https://github.com/lechiffre1/Legal-Assistant.git cd Legal-Assistant`
    
2.  **Install Dependencies**  
    Ensure Python 3.8+ is installed, then install required packages:
    
    bash
    
    CollapseWrapCopy
    
    `pip install google-generativeai langchain gradio numpy python-dotenv`
    
    _Note_: The repository doesn’t include a requirements.txt, so these are derived from typical imports in the notebook.
3.  **Set Environment Variables**  
    Obtain a Google API key and Custom Search Engine ID from [Google's Developer Console](https://developers.google.com/api-client-library/python/auth/web-app). Create a .env file in the root directory or set them in your terminal:
    
    bash
    
    CollapseWrapCopy
    
    `export GOOGLE_API_KEY='your-api-key'  export GOOGLE_CSE_ID='your-cse-id'`
    
    _Note_: On Windows, use set instead of export.
4.  **Run the Jupyter Notebook**  
    Launch the notebook to initialize the vector store and models:
    
    bash
    
    CollapseWrapCopy
    
    `jupyter notebook main/Kenyan_Legal_Assistant.ipynb`
    
    Execute all cells to load sample documents and configure the assistant.
5.  **Launch the Gradio Interface**  
    The final cell in the notebook starts the Gradio UI. Access it in your browser at the provided URL (e.g., http://127.0.0.1:7860).

## Usage

The Gradio interface provides three main tabs:

-   **Legal Research**: Enter queries like "What are the requirements for proving robbery with violence in Kenya?" to get detailed responses with case law references.
-   **Case Analysis**: Upload case text or provide a citation (e.g., from sample documents) and select "Brief" or "Comprehensive" for summaries.
-   **Document Generation**: Input client details and select a document type (e.g., petition, memo) to generate a formatted draft.

### Example Queries

Query Type

Example Query

Expected Output

Legal Research

What are the requirements for proving robbery with violence in Kenya?

Detailed explanation with case law and statutes.

Case Analysis

Text of "Case_1_Constitutional_Law.txt", Comprehensive

Structured summary with citation, facts, holding, etc.

Document Generation

Petition for land ownership dispute, client details provided

Formatted petition document ready for filing.

## Project Structure

The repository is organized as follows:

-   **main/Kenyan_Legal_Assistant.ipynb**: Core notebook with setup, logic, and Gradio UI implementation.
-   **main/sample_documents/**: Contains sample Kenyan legal documents (e.g., Case_1_Constitutional_Law.txt, Case_2_Criminal_Law.txt, Case_3_Land_Law.txt).
-   **main/example_usage.txt**: Likely contains sample queries or outputs (contents not specified).
-   **README.md**: This file.

The notebook itself is structured into sections such as:

-   Setup and API key configuration.
-   Initialization of the Gemini client and vector store.
-   Creation and embedding of sample documents.
-   Definition of search, grounding, and assistant functions.
-   Gradio UI setup and demonstration.

## Data Sources

The system uses sample Kenyan case law documents (provided in main/sample_documents/) focused on constitutional, criminal, and land law cases. These are for demonstration purposes. For production use, integrate with official sources like [Kenya Law Reports](http://kenyalaw.org).

## License

This project is for **educational purposes only** as part of a capstone project. It is not intended for production use without further development and validation.

## Further Reading

-   [Google API Key Documentation](https://developers.google.com/api-client-library/python/auth/web-app)
-   [Gradio Installation Guide](https://gradio.app/docs/installation)
-   [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction)
