# LangGraph & LangChain Advanced Concepts

[![Python Version](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/bsivavenu/langgraph_langchain?style=social)](https://github.com/bsivavenu/langgraph_langchain)
[![Last Commit](https://img.shields.io/github/last-commit/bsivavenu/langgraph_langchain)](https://github.com/bsivavenu/langgraph_langchain)

Deep dive into advanced LangGraph and LangChain concepts with practical implementations, including RAG systems, agents, state management, and production-ready patterns.

## 📚 Table of Contents

- [Overview](#-overview)
- [Core Concepts](#core-concepts)
- [Learning Path](#-learning-path)
- [Key Topics](#-key-topics)
- [Setup](#-setup)
- [Notebooks](#-notebooks)
- [Folder Structure](#-folder-structure)
- [Technologies](#-technologies)
- [Contributing](#-contributing)

## 🎯 Overview

This repository contains comprehensive tutorials and implementations of:

- **LangGraph** - Building complex autonomous agents with state graphs
- **Retrieval-Augmented Generation (RAG)** - Document-based question answering
- **Advanced Chunking & Retrieval** - Semantic, dense, sparse, and hybrid approaches
- **Agentic AI** - Building autonomous agents with reasoning capabilities
- **State Management** - DataClass and Pydantic-based state schemas
- **Tool Integration** - Connecting multiple tools to agents
- **Production Patterns** - Real-world deployment considerations

## Core Concepts

### 1. **LangGraph Fundamentals**
- State graphs and node execution
- Conditional routing and branching
- Compiled graphs for production
- Streaming and tool calling

### 2. **RAG (Retrieval-Augmented Generation)**
- Document chunking strategies
- Embedding and vector databases
- Retrieval patterns and ranking
- Reranking and refinement

### 3. **Agent Architectures**
- ReAct (Reasoning + Acting)
- Multi-tool agents
- Autonomous decision making
- Tool use and function calling

### 4. **Advanced Retrieval**
- Dense retrieval (embeddings)
- Sparse retrieval (BM25)
- Semantic chunking
- Query decomposition and expansion

### 5. **State Schemas**
- DataClass-based state
- Pydantic validation
- Complex state management
- State persistence

## 📖 Learning Path

**Recommended order for learning:**

### Beginner Level
1. **1-densesparse.ipynb** - Understand dense vs sparse retrieval
2. **1-semantichunking.ipynb** - Learn semantic chunking techniques
3. **1-queryexpansion.ipynb** - Query expansion for better retrieval
4. **2-querydecomposition.ipynb** - Breaking complex queries into simpler ones

### Intermediate Level
5. **1-simplegraph.ipynb** - Introduction to LangGraph basics
6. **2-chatbot.ipynb** - Building conversational agents
7. **2-reranking.ipynb** - Reranking retrieved documents
8. **5-ChainsLangGraph.ipynb** - Creating chains with LangGraph

### Advanced Level
9. **3-HyDE.ipynb** - Hypothetical Document Embeddings
10. **3-mmr.ipynb** - Maximum Marginal Relevance retrieval
11. **2-ReAct.ipynb** - ReAct agent pattern
12. **1-agenticrag.ipynb** - Building agentic RAG systems
13. **7-ReActAgents.ipynb** - Advanced agent implementation
14. **6-chatbotswithmultipletools.ipynb** - Multi-tool agents
15. **3-DataclassStateSchema.ipynb** - Advanced state management

### Expert Level
16. **1-streaming.ipynb** - Streaming responses
17. **3-Othervectorstores.ipynb** - Alternative vector stores
18. **PineconeVectorDB.ipynb** - Production vector database
19. **4-pydantic.ipynb** - Pydantic schemas

## 🔑 Key Topics

### Retrieval Techniques

| Technique | File | Purpose |
|-----------|------|---------|
| **Dense Retrieval** | 1-densesparse.ipynb | Embedding-based search |
| **Sparse Retrieval** | 1-densesparse.ipynb | Keyword-based search |
| **Semantic Chunking** | 1-semantichunking.ipynb | Intelligent text splitting |
| **Query Expansion** | 1-queryexpansion.ipynb | Generate alternative queries |
| **Query Decomposition** | 2-querydecomposition.ipynb | Break into sub-queries |
| **Reranking** | 2-reranking.ipynb | Improve result ranking |
| **HyDE** | 3-HyDE.ipynb | Hypothetical documents |
| **MMR** | 3-mmr.ipynb | Diversity in results |

### Agent Patterns

| Pattern | File | Use Case |
|---------|------|----------|
| **ReAct** | 2-ReAct.ipynb | Reasoning + Acting |
| **Multi-Tool** | 6-chatbotswithmultipletools.ipynb | Multiple capabilities |
| **Agentic RAG** | 1-agenticrag.ipynb | Smart document QA |
| **Chatbot** | 2-chatbot.ipynb | Conversational AI |

### State Management

| Approach | File | Details |
|----------|------|---------|
| **DataClass** | 3-DataclassStateSchema.ipynb | Simple, typed state |
| **Pydantic** | 4-pydantic.ipynb | Validated state |

### Vector Databases

| Database | File | Notes |
|----------|------|-------|
| **FAISS** | 2-faiss.ipynb | Local, fast |
| **Pinecone** | PineconeVectorDB.ipynb | Cloud, scalable |
| **Chroma** | 3-Othervectorstores.ipynb | Lightweight |

## ⚡ Setup

### Prerequisites
- Python 3.11+
- pip or uv package manager

### Installation

```bash
# Clone repository
git clone https://github.com/bsivavenu/langgraph_langchain.git
cd langgraph_langchain

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
# OR using uv
uv sync
```

### Environment Configuration

```bash
# Copy environment template
cp .env.example .env

# Add your API keys:
# - OPENAI_API_KEY
# - GOOGLE_API_KEY
# - PINECONE_API_KEY (optional)
# - Other LLM provider keys
```

## 📓 Notebooks

### LangGraph & State Management
- **1-simplegraph.ipynb** - Basic graph construction
- **1-simplegraph_1.ipynb** - Graph variations
- **3-DataclassStateSchema.ipynb** - DataClass state management
- **4-pydantic.ipynb** - Pydantic validation
- **5-ChainsLangGraph.ipynb** - Building chains
- **1-streaming.ipynb** - Real-time response streaming

### RAG & Retrieval
- **1-densesparse.ipynb** - Dense vs sparse retrieval
- **1-semantichunking.ipynb** - Semantic chunking
- **1-queryexpansion.ipynb** - Query expansion techniques
- **2-querydecomposition.ipynb** - Query decomposition
- **2-reranking.ipynb** - Reranking strategies
- **3-HyDE.ipynb** - Hypothetical document embeddings
- **3-mmr.ipynb** - Maximum marginal relevance

### Agents
- **2-ReAct.ipynb** - ReAct agent pattern
- **2-ReAct (1).ipynb** - ReAct variations
- **1-agenticrag.ipynb** - Agentic RAG system
- **7-ReActAgents.ipynb** - Advanced agent implementation
- **6-chatbotswithmultipletools.ipynb** - Multi-tool chatbot

### Vector Stores & Embeddings
- **embedding.ipynb** - Embedding fundamentals
- **embedding_1.ipynb** - Advanced embeddings
- **2-faiss.ipynb** - FAISS vector store
- **PineconeVectorDB.ipynb** - Pinecone integration
- **3-Othervectorstores.ipynb** - Alternative databases

### Chatbots
- **2-chatbot.ipynb** - Basic chatbot implementation

### Additional Resources
- **0-DataIngestParsing/** - Data parsing and ingestion folder

## 📁 Folder Structure

```
langgraph_langchain/
├── README.md                          # This file
├── CONTRIBUTING.md                    # Contribution guidelines
├── GITHUB_ACTIONS_GUIDE.md           # CI/CD documentation
├── COMPLETE_QA_GUIDE.md              # FAQ and Q&A
├── .env.example                       # Environment template
├── pyproject.toml                     # Project configuration
├── requirements.txt                   # Dependencies
├── uv.lock                           # Dependency lock file
│
├── 📓 Core Notebooks/
│   ├── 1-simplegraph.ipynb
│   ├── 1-simplegraph_1.ipynb
│   ├── 3-DataclassStateSchema.ipynb
│   ├── 4-pydantic.ipynb
│   ├── 5-ChainsLangGraph.ipynb
│   └── 1-streaming.ipynb
│
├── 🔍 Retrieval & RAG/
│   ├── 1-densesparse.ipynb
│   ├── 1-semantichunking.ipynb
│   ├── 1-queryexpansion.ipynb
│   ├── 2-querydecomposition.ipynb
│   ├── 2-reranking.ipynb
│   ├── 3-HyDE.ipynb
│   ├── 3-mmr.ipynb
│   └── 1-agenticrag.ipynb
│
├── 🤖 Agents/
│   ├── 2-ReAct.ipynb
│   ├── 2-ReAct (1).ipynb
│   ├── 7-ReActAgents.ipynb
│   ├── 2-chatbot.ipynb
│   └── 6-chatbotswithmultipletools.ipynb
│
├── 📦 Vector Stores/
│   ├── embedding.ipynb
│   ├── embedding_1.ipynb
│   ├── 2-faiss.ipynb
│   ├── PineconeVectorDB.ipynb
│   └── 3-Othervectorstores.ipynb
│
├── 📂 0-DataIngestParsing/
│   ├── 1-dataingestion.ipynb
│   ├── 2-dataparsingpdf.ipynb
│   ├── 3-dataparsingdoc.ipynb
│   ├── 4-csvexcelparsing.ipynb
│   ├── 5-jsonparsing.ipynb
│   ├── 6-databaseparsing.ipynb
│   └── data/
│
├── 📚 Resources/
│   ├── PDF guides and references
│   ├── research_notes.txt
│   ├── sample_docs.txt
│   └── langchain_*.txt datasets
│
├── 📊 Output/
│   └── (Generated outputs)
│
└── 🔧 Configuration/
    ├── .env
    ├── .env.example
    ├── .gitignore
    └── .github/workflows/
```

## 🛠 Technologies

### Core Frameworks
- **LangChain** - LLM orchestration framework
- **LangGraph** - Stateful graph computation
- **FastAPI** - Web framework (when needed)

### LLM Providers
- **OpenAI** - GPT models
- **Google Generative AI** - Gemini models
- **Groq** - Fast inference
- **HuggingFace** - Open source models

### Vector Databases
- **FAISS** - Local embeddings
- **Pinecone** - Cloud vector DB
- **Chroma** - Lightweight vector store

### Data Processing
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Pydantic** - Data validation

### Document Processing
- **pypdf** - PDF parsing
- **docx2txt** - Word document parsing
- **BeautifulSoup** - HTML parsing

## 🚀 Quick Start

### Run a Notebook

```bash
# Start Jupyter
jupyter notebook

# Open any notebook to explore
```

### Example: Query a Document

```python
from langchain import OpenAI
from langchain.vectorstores import FAISS

# Initialize
llm = OpenAI(api_key="sk-...")
vectorstore = FAISS.from_documents(...)

# Query
response = vectorstore.similarity_search("Your question")
```

## 📖 Core Concepts Explained

### What is LangGraph?
LangGraph is a library for building stateful, agentic applications with LLMs. It provides:
- Graph-based control flow
- State management
- Tool calling and streaming
- Compiled graphs for production

### What is RAG?
Retrieval-Augmented Generation combines:
- Document retrieval (searching relevant docs)
- Generation (creating answers with context)
- Provides current, accurate, specific information

### What is an Agent?
An autonomous entity that:
- Observes the environment
- Takes reasoning steps
- Calls tools to accomplish tasks
- Iterates until goal is reached

## 📚 Resources

### Documentation
- [LangChain Docs](https://python.langchain.com/)
- [LangGraph Docs](https://langchain-ai.github.io/langgraph/)
- [OpenAI API](https://platform.openai.com/docs)
- [Google AI Studio](https://makersuite.google.com/)

### PDFs & Guides (in this repo)
- 1-+AI+agents+vs+agentic+AI.pdf - Agent concepts
- 18-Agents.pdf - Agent implementation
- 35-39-RAGS.pdf - RAG comprehensive guide
- And many more...

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md)

### How to Contribute
1. Fork the repository
2. Create a feature branch
3. Add your notebooks/improvements
4. Submit a pull request

### Guidelines
- Include descriptive comments
- Add markdown cells explaining concepts
- Test before submitting
- Follow existing naming conventions

## ⚠️ .env Configuration

**Important:** Never commit `.env` file with actual API keys!

1. Copy `.env.example` to `.env`
2. Add your actual API keys
3. `.env` is in `.gitignore` - it won't be committed

### Required Environment Variables
```env
OPENAI_API_KEY=sk-...
GOOGLE_API_KEY=...
PINECONE_API_KEY=... (optional)
PINECONE_ENVIRONMENT=... (optional)
```

## 🔄 GitHub Actions

This repository has automated testing and linting via GitHub Actions. See [GITHUB_ACTIONS_GUIDE.md](GITHUB_ACTIONS_GUIDE.md) for details.

## ❓ FAQ

See [COMPLETE_QA_GUIDE.md](COMPLETE_QA_GUIDE.md) for comprehensive Q&A.

## 📊 Project Statistics

- 📓 **26 Jupyter Notebooks**
- 📁 **1 Data Parsing Folder** with 6 notebooks
- 📚 **15+ PDF References**
- 🛠 **20+ Dependencies**
- 💾 **Comprehensive coverage** of advanced concepts

## 🏆 Key Features

✅ Production-ready patterns
✅ Comprehensive documentation
✅ Multiple agent architectures
✅ Advanced retrieval techniques
✅ Vector database integrations
✅ State management patterns
✅ Real-world examples

## 📈 Learning Outcomes

After working through this repository, you'll understand:

- How to build LangGraph applications
- Implementing RAG systems effectively
- Creating autonomous agents with reasoning
- Advanced document retrieval techniques
- State management and persistence
- Tool integration and function calling
- Production deployment considerations

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details

## 🙏 Acknowledgments

Built with:
- [LangChain](https://www.langchain.com/)
- [LangGraph](https://langchain-ai.github.io/langgraph/)
- [OpenAI](https://openai.com/)
- [Google AI](https://ai.google/)
- [Pinecone](https://www.pinecone.io/)

---

**Repository:** https://github.com/bsivavenu/langgraph_langchain  
**Last Updated:** February 2, 2026  
**Status:** ✅ Active & Maintained
