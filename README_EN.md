# Intelligent Customer Service Robot System

A RAG (Retrieval-Augmented Generation) based intelligent customer service system with Streamlit web interface.

## Project Overview

This is an intelligent customer service system based on RAG (Retrieval-Augmented Generation) technology. It integrates large language models, vector databases, and intelligent agents to retrieve relevant information from knowledge bases and generate accurate responses based on user queries.

## Key Features

- **Intelligent Q&A**: RAG-based question-answering system that can retrieve relevant information from document libraries
- **Multi-tool Integration**: Integrated with various tools including weather queries, user location, user ID retrieval, etc.
- **Real-time Monitoring**: Built-in tool call monitoring and logging capabilities
- **Streaming Response**: Supports streaming output for better user experience
- **Web Interface**: Modern web interface based on Streamlit

## Technology Stack

- **Python 3.8+**
- **Streamlit**: Web application framework
- **LangChain**: LLM application development framework
- **ChromaDB**: Vector database
- **Large Language Models**: Supports multiple LLM models

## Project Structure

```
├── agent/               # Intelligent agent module
│   ├── react_agent.py   # React agent implementation
│   └── tools/           # Tool functions
├── rag/                 # RAG service module
│   ├── rag_service.py   # RAG service implementation
│   └── vector_store.py  # Vector storage service
├── config/              # Configuration files
│   ├── agent.yml        # Agent configuration
│   ├── rag.yml          # RAG configuration
│   ├── chroma.yml       # ChromaDB configuration
│   └── prompts.yml      # Prompt configuration
├── model/               # Model related
├── utils/               # Utility functions
├── data/                # Data files
├── logs/                # Log files
├── app.py               # Streamlit application entry point
└── main.py              # Main program
```

## Quick Start

### Requirements

- Python 3.8 or higher
- pip package manager

### Installation Steps

1. **Clone the project**
   ```bash
   git clone <repository-url>
   cd RAG_Project
   ```

2. **Create virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   # or
   .venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   Create `.env` file and configure necessary API keys:
   ```
   # LLM API Configuration
   OPENAI_API_KEY=your_api_key
   # or other model API keys
   ```

5. **Start the application**
   ```bash
   streamlit run app.py
   ```

## Configuration Guide

### Model Configuration
Configure various model parameters in the `config/` directory:
- `agent.yml`: Intelligent agent configuration
- `rag.yml`: RAG service configuration
- `prompts.yml`: System prompt configuration

### Vector Database
Uses ChromaDB as vector storage, configured in `config/chroma.yml`.

## Usage Instructions

1. After starting the application, access the displayed URL in your browser
2. Enter questions in the chat interface
3. The system will automatically retrieve relevant knowledge and generate responses
4. You can view the response generation process in real-time

## Development Guide

### Adding New Tools

Create new tool functions in the `agent/tools/` directory, then import and use them in `react_agent.py`.

### Customizing Prompts

Modify the `config/prompts.yml` file to customize system prompts.

### Expanding Knowledge Base

Add documents to the `data/` directory, and the system will automatically process and create vector indexes.

## Contribution Guidelines

1. Fork the project
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Contact

For questions or suggestions, please submit an Issue or contact the project maintainers.