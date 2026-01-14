# 🤝 Contributing Guide

Thank you for considering contributing to Extract PDF! This document provides guidelines to make the contribution process as smooth as possible.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Environment Setup](#development-environment-setup)
- [Development Process](#development-process)

## 📜 Code of Conduct

This project adheres to a code of conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior through GitHub issues.

### Our Values

- **Respect**: Treat everyone with respect and consideration
- **Collaboration**: Work together to achieve the best results
- **Transparency**: Communicate openly about decisions and changes
- **Quality**: Maintain high standards of code and documentation

## 🚀 How Can I Contribute?

### Contributing Code

1. **Fork the repository**
2. **Create a branch** for your feature
3. **Make your changes**
4. **Write/update tests**
5. **Update documentation**
6. **Submit a Pull Request**

## 🛠️ Development Environment Setup

### 1. Fork and Clone

```bash
# Fork on GitHub, then clone your fork
git clone https://github.com/YOUR-USERNAME/extract-pdf.git
cd extract-pdf

# Add the original repository as upstream
git remote add upstream https://github.com/ORIGINAL-USERNAME/extract-pdf.git
```

### 2. Set Up Virtual Environment

```bash
# Create virtual environment
python -m venv .venv

# Activate environment
source .venv/bin/activate  # Linux/Mac
# or
.venv\Scripts\activate  # Windows
```

### 3. Install Development Dependencies

```bash
# Install project in development mode
pip install -e ".[dev]"
```

### 4. Set Up Database

```bash
# Start PostgreSQL (example with Docker)
docker run -d \
  --name extract-pdf-db \
  -e POSTGRES_PASSWORD=postgres \
  -e POSTGRES_DB=extract_pdf \
  -p 5432:5432 \
  pgvector/pgvector:pg16

# Create pgvector extension
psql -h localhost -U postgres -d extract_pdf -c "CREATE EXTENSION IF NOT EXISTS vector;"
```

## 🔄 Development Process

### Branch Workflow

- `main`: Main branch, always stable
- `develop`: Development branch
- `feature/feature-name`: New features
- `bugfix/bug-name`: Bug fixes
- `hotfix/hotfix-name`: Urgent fixes

### Creating a Branch

```bash
# Update your repository
git checkout main
git pull upstream main

# Create a new branch
git checkout -b feature/my-feature
```

### Making Commits

Use clear and descriptive commit messages:

```bash
# Recommended format
git commit -m "type: short description

More detailed description if needed.

Fixes #123"
```

**Commit types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Formatting, missing semicolons, etc
- `refactor`: Code refactoring
- `test`: Adding or fixing tests
- `chore`: Maintenance tasks

## 🎯 Priority Areas

We are especially interested in contributions in the following areas:

### High Priority
- 🔥 OCR support for scanned PDFs
- 🔥 Performance optimization for large PDFs
- 🔥 Web interface for PDF upload

### Medium Priority
- ⭐ Support for more formats (DOCX, TXT, HTML)
- ⭐ Metrics dashboard
- ⭐ Integration examples with chatbots

### Low Priority
- 💡 Documentation improvements
- 💡 More integration tests

## 💬 Communication

- **Issues**: For bugs and feature requests
- **Discussions**: For questions and general discussions
- **Pull Requests**: For code contributions

## 🙏 Recognition

All contributors will be recognized in the README.md and CONTRIBUTORS.md file.

---

**Thank you for contributing! 🎉**
