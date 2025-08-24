# Research-agent-End-to-End-local-Agentic-RAG-system-
This project is an advanced, end-to-end, and fully local AI agent system designed for automated research discovery. It leverages a powerful tech stack including CrewAI, Ollama, and OpenSearch to analyze real-time patent and research data, identify emerging trends, and generate comprehensive summary reports.

(Note: The demo video must be downloaded to be viewed due to its size.)

# Overview
This system automates the complex process of research and analysis. It uses an autonomous multi-agent framework to dynamically decompose tasks, retrieve relevant information from patent databases, perform in-depth analysis, and deliver actionable insights. The entire pipeline, from data retrieval to analysis, runs locally, ensuring data privacy and control.

The core retrieval-augmented generation (RAG) pipeline is equipped with multiple search strategies—semantic, keyword, and hybrid—to ensure the highest quality and relevance of retrieved data.

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

# Agents created in project 
- research director
- patent retriever
- data analyst
- innovation forcaster

# knowledge and retrieval 
- Semantic Search
- Keyword Search               
- Hybrid Search

# File Structure
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

# Prerequisites
Before you begin, ensure you have the following installed:
- Python 3.10+
- Docker and Docker Compose
- Ollama
- You will also need a SerpAPI key to fetch patent data.


# Installation and Setup
Follow these steps to get the project running on your local machine.
1. Clone the Repository
```
git clone https://github.com/DhruvShah510/Research-agent-End-to-End-local-Agentic-RAG-system-.git
```
2. Set Up Virtual Environment
```
python -m venv .venv
source .venv/bin/activate  # On Windows, use `.venv\Scripts\activate`
```
3. Install Dependencies
```
pip install -r requirements.txt
```
4. Configure Environment Variables
   
Create a .env file in the root directory and add your SerpAPI key:
```
SERPAPI_API_KEY="your_serpapi_key_here"
```

5. Start Services with Docker
   
This single command will start the OpenSearch and OpenSearch Dashboards services.
Note : run the command in the terminal and set the path of the docker-compse.yml file properly
```
docker compose -f docker-compose.yml up 
You can check if OpenSearch is running by visiting http://localhost:9200.
```

6. Set Up Ollama and Download Models
   
Ensure Ollama image is installed in docker and running. Then, pull the required LLM and embedding models:
```
docker exec -it ollama ollama run deepseek-r1:1.5b 
docker exec -it ollama ollama pull nomic-embed-text
```

# Usage
The workflow is divided into two main steps: data collection and analysis.

1. Collect and Ingest Data :
   
Run the information_collector.py script to fetch patent data from Google Patents via SerpAPI. This script will automatically create embeddings and ingest them into your OpenSearch instance.

```
python information_collector.py
```

2. Run the Research Agent :
   
Execute the main application file to start the agentic workflow. The agents will begin their research and analysis based on the predefined query in the script.

```
python agentic_rag.py
```

Upon completion, a detailed report file named patent_analysis_...txt will be generated in the root directory.

# Author:
Dhruv Shah


