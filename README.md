#  Extract PDF - RAG-Powered Document Intelligence

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![LangChain](https://img.shields.io/badge/LangChain-Enabled-green.svg)](https://www.langchain.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-pgvector-blue.svg)](https://github.com/pgvector/pgvector)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **Intelligent extraction of information from PDF manuals at scale to power RAG-based chatbots**

##  Overview

This project was born from the need to extract information from large volumes of PDF manuals efficiently and in a structured way. Using **LangChain's** vector storage abstraction with **PostgreSQL** and the **pgvector** extension, the system processes PDF documents and transforms them into vector embeddings, enabling advanced semantic search to power intelligent chatbots.

###  Key Features

-  **Batch Processing**: Automated extraction of multiple PDFs simultaneously
-  **Vector Embeddings**: Text conversion into vector representations for semantic search
-  **PostgreSQL + pgvector**: Scalable and efficient vector storage
-  **RAG Ready**: Direct integration with chatbot systems using Retrieval-Augmented Generation
-  **LangChain Integration**: Uses robust LangChain abstractions for document management
-  **Performance**: Optimized for processing large volumes of technical documentation

##  Quick Start

### Prerequisites

- Python 3.10 or higher
- PostgreSQL 12+ with pgvector extension
- pip or uv for package management

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ManuelPauloAfonso/extract_pdf.git
   cd extract-pdf
   ```

2. **Set up virtual environment**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -e .
   ```

4. **Configure PostgreSQL with pgvector**
   ```sql
   CREATE EXTENSION IF NOT EXISTS vector;
   ```

5. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit the .env file with your credentials
   ```

##  Contributing

Contributions are very welcome! This project is under active development and there are many opportunities for improvements.

### How to Contribute

1. **Fork the project**
2. **Create a feature branch** (`git checkout -b feature/MyFeature`)
3. **Commit your changes** (`git commit -m 'Add MyFeature'`)
4. **Push to the branch** (`git push origin feature/MyFeature`)
5. **Open a Pull Request**

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [LangChain](https://www.langchain.com/) for the excellent vector storage abstraction
- [pgvector](https://github.com/pgvector/pgvector) for the PostgreSQL vector extension
- Open source community for tools and inspiration

## 📧 Contact

- **GitHub**: [ManuelPauloAfonso/extract_pdf](https://github.com/ManuelPauloAfonso/extract_pdf)
- **LinkedIn**: [Manuel Paulo Afonso](https://www.linkedin.com/in/manuelpauloafonso/)
- **Issues**: [GitHub Issues](https://github.com/ManuelPauloAfonso/extract_pdf/issues)

---

**Developed with ❤️ to make knowledge in PDFs accessible via AI**
