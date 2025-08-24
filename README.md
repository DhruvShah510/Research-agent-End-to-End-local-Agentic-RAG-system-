# Research-agent-End-to-End-local-Agentic-RAG-system-
This project is an advanced, end-to-end, and fully local AI agent system designed for automated research discovery. It leverages a powerful tech stack including CrewAI, Ollama, and OpenSearch to analyze real-time patent and research data, identify emerging trends, and generate comprehensive summary reports.

(Note: The demo video must be downloaded to be viewed due to its size.)

# Overview
This system automates the complex process of research and analysis. It uses an autonomous multi-agent framework to dynamically decompose tasks, retrieve relevant information from patent databases, perform in-depth analysis, and deliver actionable insights. The entire pipeline, from data retrieval to analysis, runs locally, ensuring data privacy and control.

The core retrieval-augmented generation (RAG) pipeline is equipped with multiple search strategies—semantic, keyword, and hybrid—to ensure the highest quality and relevance of retrieved data.

# System Architecture
The project is built on a multi-layered architecture that ensures a clear separation of concerns, from data storage to agentic task execution.

Of course. Here is how you can fix the spacing and alignment issues in your `README.md` file.

The solution for both problems is to use **Markdown code blocks**. When you wrap text in a code block, it uses a monospaced font, which means every character has the same width. This preserves all your spaces and keeps text-based diagrams perfectly aligned.

-----

### 1\. Aligning the File Structure Comments

To create a clean, table-like look, wrap the entire file list in a fenced code block (using three backticks ` ``` `) and then manually add spaces to align the `#` comments.

**Replace this:**

  * `agentic_rag.py # Main application entry point`
  * `patent_crew.py # Defines CrewAI agents, tools, and tasks`
  * ...and so on

**With this:**

```
├── agentic_RAG_demo.mp4     # Project demo video
├── agentic_rag.py           # Main application entry point
├── patent_crew.py           # Defines CrewAI agents, tools, and tasks
├── patent_search_tools.py   # Contains search functions (semantic, keyword, hybrid)
├── information_collector.py # Fetches patent data using SerpAPI
├── helper.py                # Helper functions for data collection
├── embeddings.py            # Handles text embedding generation
├── ingestion.py             # Ingests embeddings into OpenSearch
├── opensearch_client.py     # OpenSearch client configuration
├── docker-compose.yml       # Docker configuration for OpenSearch services
├── requirements.txt         # Python dependencies
└── dev.ipynb                # Jupyter notebook for development and testing
```

*I've used the `├──` and `└──` characters to give it a nice tree structure, which is common practice.*

-----

### 2\. Fixing the System Architecture Diagram

Your diagram is misaligned because standard text uses proportional fonts. Wrapping it in a code block will force a monospaced font and fix the alignment.

Here is a corrected and slightly cleaned-up version of your architecture diagram that you can copy and paste directly into your `README.md`.

**Replace your current broken diagram with this:**

```
┌──────────────────────────────────┐
│          User Interface          │
│ (Input Query via Terminal)       │
└──────────────────────────────────┘
                 │
                 ▼
┌──────────────────────────────────┐
│      Agent Orchestration         │
│             (CrewAI)             │
│   - Research Director Agent      │
│   - Patent Retriever Agent       │
│   - Data Analyst Agent           │
└──────────────────────────────────┘
                 │
                 ▼
┌──────────────────────────────────┐
│      Knowledge & Retrieval       │
│     (Custom Search Tools)        │
│   - Semantic Search              │
│   - Keyword Search               │
│   - Hybrid Search                │
└──────────────────────────────────┘
                 │
                 ▼
┌──────────────────────────────────┐
│      Data Storage & Indexing     │
│           (OpenSearch)           │
└──────────────────────────────────┘
```


# Key Features
- Autonomous Multi-Agent System: Utilizes CrewAI to create specialized AI agents for research direction, data retrieval, and analysis.
- Local First: Runs entirely on your local machine using Ollama for language models, ensuring privacy and offline capabilities.
- Advanced RAG Pipeline: Implements semantic, keyword, and hybrid search methods to query vectorized data stored in OpenSearch.
- Real-Time Data Sourcing: Fetches the latest patent and research data using the SerpAPI integration.
- End-to-End Automation: From data collection and embedding creation to final report generation, the entire workflow is automated.

# Tech Stack
- Agent Framework: CrewAI
- Local LLMs: Ollama
- Vector Database: OpenSearch
- LLM Model: deepseek-r1:1.5b
- Embedding Model: nomic-embed-text
- Data API: SerpAPI (for Google Patents)

# File Structure
A brief overview of the key files in this repository:
- agentic_RAG_demo.mp4      ```  # Project demo video
- agentic_rag.py            ```  # Main application entry point
- patent_crew.py              # Defines CrewAI agents, tools, and tasks
- tent_search_tools.py        # Contains search functions (semantic, keyword, hybrid)
- information_collector.py    # Fetches patent data using SerpAPI
- helper.py                   # Helper functions for data collection
- embeddings.py               # Handles text embedding generation
- ingestion.py                # Ingests embeddings into OpenSearch
- opensearch_client.py        # OpenSearch client configuration
- docker-compose.yml          # Docker configuration for OpenSearch services
- requirements.txt            # Python dependencies
- dev.ipynb                   # Jupyter notebook for development and testing


# Prerequisites
Before you begin, ensure you have the following installed:
- Python 3.10+
- Docker and Docker Compose
- Ollama
- You will also need a SerpAPI key to fetch patent data.


# Installation and Setup
Follow these steps to get the project running on your local machine.
1. Clone the Repository


