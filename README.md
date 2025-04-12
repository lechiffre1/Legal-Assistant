# Multilingual Legal Assistant

A comprehensive AI-powered toolkit for legal queries, case analysis, document generation, and clause extraction across both Kenyan and German legal systems. Built as a capstone project for the Google & Kaggle 5-Day Generative AI Workshop in Q1 2025.

## ✨ Features

-   **Legal Query**: Ask jurisdiction-specific legal questions in English or German and receive accurate, contextual responses.
-   **Case Analysis**: Analyze case law with customizable detail levels, search for specific cases, or upload case documents for AI-powered examination.
-   **Document Generation**: Create professionally formatted legal documents tailored to Kenyan or German conventions and requirements.
-   **Clause Analysis**: Extract and analyze clauses from legal documents by uploading PDFs for AI-powered structure recognition.

## 🏗️ Technologies Used

-   **Google Gemini API**: Uses gemini-2.0-flash or falls back to gemini-1.5-flash for natural language generation and reasoning
-   **Vector Embeddings**: Implements both Chroma (primary) and a custom SimpleVectorStore (fallback) for semantic search
-   **PyPDF2**: Processes uploaded PDFs for clause extraction and document analysis
-   **LangChain**: Orchestrates AI workflows with Google's Generative AI embeddings
-   **Gradio**: Provides a simple intuitive, tab-based UI with jurisdiction selection

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/lechiffre1/Legal-Assistant.git
cd Legal-Assistant

```

### 2. Install Dependencies

Ensure Python 3.8+ is installed, then run:

```bash
pip install google-generativeai langchain-google-genai langchain gradio numpy PyPDF2 requests

```

### 3. Set API Credentials

Obtain a Google Gemini API key and optional Google Custom Search Engine ID:

```bash
export GOOGLE_API_KEY='your-gemini-api-key'
export GOOGLE_CSE_ID='your-search-id'  # Optional for web search functionality

```

On Windows, use `set` instead of `export`.

### 4. Run the Application

```bash
python app.py

```

This builds sample vector stores for both jurisdictions and starts the Gradio UI.

### 5. Access the Gradio UI

Visit the provided URL (typically http://127.0.0.1:7860) to use the interface.

## 🎯 Usage

Select Kenya or Germany in the interface, then choose a feature:

Tab

Example Input

Expected Output

Legal Query

"What are the data protection laws in Kenya?"

Jurisdiction-specific legal explanation with citations

Case Analysis

Upload a PDF of a court decision or enter case text

Structured analysis of the case with key findings

Document Generator

Select "Lease Agreement" and provide details

Formatted legal document following jurisdiction standards

Clause Analysis

Upload a contract or agreement PDF

Extracted clauses with page references and analysis

## 🖥️ Implementation Highlights

-   **Fault-Tolerant Vector Storage**: Falls back to SimpleVectorStore when Chroma isn't available
-   **Multi-Format Document Processing**: Handles both text and PDF uploads across features
-   **Jurisdiction-Aware Responses**: Adapts content to either common law (Kenya) or civil law (Germany) contexts
-   **Expandable Document Templates**: Includes jurisdiction-specific document types with appropriate formatting

## 🚦 Limitations & Troubleshooting

-   **API Quotas**: You may encounter quota limitations with the free tier of Google's Gemini API
-   **Sample Data**: Currently includes limited sample legal documents; expand with your own jurisdiction-specific content
-   **Error Handling**: System role errors can occur with certain API versions; the application includes fallbacks
-   **Memory Usage**: Processing large PDFs may require additional memory allocation

## 🏆 Author

Jasper Michieka

-   LinkedIn: jasper-michieka

Developed for Google & Kaggle's 5-Day GenAI Workshop, Q1 2025.

## 🤝 License

MIT License. For educational purposes only as a capstone project. No warranty. Not official legal advice.


