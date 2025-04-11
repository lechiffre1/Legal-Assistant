# Legal Assistant for Kenyan and German Lawyers 🇰🇪🇩🇪⚖️

**A Gemini-Powered Toolkit for Legal Research, Summarization, and Drafting Across Jurisdictions**

This AI-driven legal assistant empowers professionals in **Kenya** and **Germany** to research case law, generate summaries, and draft documents. Built as a capstone for the **Google & Kaggle 5-Day Generative AI Course in Q1 2025**, it bridges common law and civil law systems with advanced AI.

----------

## ✨ Features

-   **Multilingual Legal Research**: Search and analyze Kenyan and German case law using vector embeddings and optional Google Search grounding.
-   **Case Summarization**: Generate structured summaries (brief or comprehensive) for cases in both jurisdictions.
-   **Document Generation**: Create professionally formatted legal documents following Kenyan or German conventions.
-   **Comparative Analysis**: Research and compare legal concepts across the two systems (e.g., contract law in BGB vs. Kenyan statutes).

----------

## 🏗️ Technologies Used

-   **Google Gemini 2.5 Pro**: Powers natural language generation and analysis.
-   **Vector Embeddings**: Custom SimpleVectorStore for semantic search across jurisdictions.
-   **LangChain**: Orchestrates AI workflows and document management.
-   **LangGraph**: Enables agent-based task handling.
-   **RAG (Retrieval-Augmented Generation)**: Ensures grounded, jurisdiction-specific responses.
-   **Gradio**: Delivers an interactive, multilingual UI.

----------

## 🚀 Quick Start

### 1. Clone the Repository

bash

CollapseWrapCopy

`git clone https://github.com/lechiffre1/Legal-Assistant.git cd Legal-Assistant`

### 2. Install Dependencies

Ensure Python 3.8+ is installed, then run:

bash

CollapseWrapCopy

`pip install google-generativeai langchain gradio numpy python-dotenv`

_Note_: Core packages; expand as needed for German data integration.

### 3. Set API Credentials

Obtain a [Google Gemini API key](https://developers.google.com/api-client-library/python/auth/web-app) and optional [Google Custom Search Engine ID](https://programmablesearchengine.google.com/). Set them:

bash

CollapseWrapCopy

`export GOOGLE_API_KEY='your-gemini-api-key'  export GOOGLE_CSE_ID='your-search-id'  # Optional for live search`

_On Windows, use set instead of export._

### 4. Run the Notebook

Launch and execute all cells:

bash

CollapseWrapCopy

`jupyter notebook main/Kenyan_Legal_Assistant.ipynb`

Builds sample vector stores for both jurisdictions and starts the Gradio UI.

### 5. Access the Gradio UI

Visit the provided URL (e.g., http://127.0.0.1:7860) to select a jurisdiction and use the features.

----------

## 🎯 Usage

Select **Kenya** or **Germany** in the Gradio interface, then choose a feature:

Feature

Example Query/Input

Expected Output

Legal Research

"Requirements for robbery in Kenya" or "§ 249 StGB Raub"

Jurisdiction-specific legal explanation.

Case Summarization

Text of Case_1_Constitutional_Law.txt or a BGH ruling

Structured summary with facts, holding, citation.

Document Generation

Petition for land dispute (Kenya) or Kündigung (Germany)

Formatted document per local standards.

Comparative Analysis

"Contract validity in Kenya vs. Germany"

Side-by-side comparison of legal principles.

-   **Legal Research**: Ask jurisdiction-specific questions.
-   **Case Analysis**: Analyze cases with adjustable detail levels.
-   **Document Generation**: Draft documents tailored to each system.
-   **Comparative Analysis**: Compare legal topics across Kenya and Germany.

----------

## 🗃️ Project Structure

-   **main/Kenyan_Legal_Assistant.ipynb**: Core notebook with setup, logic, and UI (adaptable for Germany).
-   **main/sample_documents/**: Sample Kenyan cases (e.g., Case_1_Constitutional_Law.txt); add German equivalents.
-   **main/example_usage.txt**: Sample queries or outputs.
-   **README.md**: This file.

Notebook sections include:

-   Setup and API configuration.
-   Vector store creation for both jurisdictions.
-   Jurisdiction-specific functions (search, analysis, drafting).
-   Gradio UI with jurisdiction selector.

----------

## 🖥️ Demo Screenshot

![Gradio UI](https://github.com/lechiffre1/Legal-Assistant/blob/main/demo_screenshot.png)  
_Tabs for Kenyan and German legal tasks, plus comparative analysis._

----------

## 📚 Data Sources

-   **Kenya**: Sample cases in main/sample_documents/; extend with [Kenya Law Reports](http://kenyalaw.org).
-   **Germany**:
    -   [Open Legal Data API](https://de.openlegaldata.io) for free case law (API key required).
    -   [Gesetze-im-Internet.de](https://www.gesetze-im-internet.de) for statutes (scrape or download).
    -   Optional: [Rechtsprechung-im-Internet.de](https://www.rechtsprechung-im-internet.de) for federal rulings.

----------

## ⚙️ Implementation Highlights

-   **Multilingual RAG**: Combines Kenyan and German vector stores with optional Google Search.
-   **Function Calling**: Gemini invokes jurisdiction-aware functions (e.g., analyze_case_law_de).
-   **Sample Data**: Kenyan cases included; German data to be added (e.g., BGB, BGH rulings).
-   **UI**: Gradio tabs with a jurisdiction dropdown.

----------

## 🚦 Limitations & Next Steps

-   **Sample Data**: Limited to Kenyan samples; German data requires integration.
-   **Verification**: Outputs need legal review per jurisdiction.
-   **Future Plans**: Add Swahili and German language support, connect to official APIs, refine comparative analysis.

----------

## 🏆 Author

**Jasper Michieka**

-   LinkedIn: [jasper-michieka](https://www.linkedin.com/in/jasper-michieka/)
-   Email: [jasper.michieka@mail.com](mailto:jasper.michieka@mail.com)

Developed for Google & Kaggle’s 5-Day GenAI Bootcamp, Q1 2025.

----------

## 🤝 License

MIT License. For **educational purposes only** as a capstone project. No warranty. **Not official legal advice.**

----------

## 🇰🇪🇩🇪 Bridging Legal Systems with AI

Empowering lawyers in Kenya and Germany—questions? Reach out above!
