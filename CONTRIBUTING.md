# Contributing to LangGraph LangChain Advanced

Thank you for your interest in contributing! This document provides guidelines for contributing to this repository.

## Code of Conduct

Please be respectful and constructive in all interactions. We aim to maintain a welcoming community.

## Getting Started

### 1. Fork & Clone
```bash
git clone https://github.com/YOUR_USERNAME/langgraph_langchain.git
cd langgraph_langchain
```

### 2. Set Up Environment
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
uv sync  # or: pip install -r requirements.txt
```

### 3. Create Feature Branch
```bash
git checkout -b feature/your-feature-name
```

## Development Guidelines

### For Jupyter Notebooks

1. **Clear Structure**
   - Use markdown cells to explain concepts
   - Include section headers
   - Break into logical cells

2. **Code Quality**
   - Use meaningful variable names
   - Add comments for complex logic
   - Test cells before committing

3. **Documentation**
   - Explain what each notebook teaches
   - Include imports at the top
   - Show expected outputs

4. **Naming Convention**
   - Use descriptive names: `topic-description.ipynb`
   - Follow existing pattern: `1-topic.ipynb`, `2-topic.ipynb`

### Commit Messages

```
feat: Add new notebook on topic X
fix: Correct implementation in notebook Y
docs: Update README with new content
refactor: Improve notebook structure
```

### Pull Request Process

1. **Before Submitting**
   - Run all notebook cells
   - Verify code works
   - Update README if needed

2. **PR Title & Description**
   ```markdown
   ## Description
   Brief description of what notebook/changes you're adding
   
   ## Type
   - [ ] New notebook
   - [ ] Documentation update
   - [ ] Bug fix
   - [ ] Enhancement
   
   ## Related Files
   - notebook-name.ipynb
   ```

3. **Review Process**
   - Maintainers will review
   - Be responsive to feedback
   - Make requested changes

## Adding a New Notebook

### Structure Template

```python
# Cell 1: Title & Overview
# # [Topic Title]
# 
# This notebook covers:
# - Concept 1
# - Concept 2
# - Concept 3

# Cell 2: Imports
import os
from langchain import OpenAI
from langchain.vectorstores import FAISS
# ... other imports

# Cell 3: Setup
from dotenv import load_dotenv
load_dotenv()
api_key = os.getenv("OPENAI_API_KEY")

# Cell 4: Main Content
# Organized sections with markdown & code

# Cell 5: Examples
# Practical usage examples

# Cell 6: Summary
# Key takeaways
```

### Notebook Organization

- **Root level notebooks**: Core concepts, one-off topics
- **0-DataIngestParsing/**: Data loading and parsing techniques
- **Naming**: Follow existing pattern (1-, 2-, 3-, etc.)

## Environment Variables

- Never commit `.env` with actual keys
- Use `.env.example` as template
- Document required variables

## Best Practices

1. **Test Before Submitting**
   - Run all cells in order
   - No errors or warnings
   - Clear output examples

2. **Documentation**
   - Clear explanations of concepts
   - Comments in code
   - Example usage

3. **Keep It Simple**
   - One topic per notebook
   - Focused content
   - Avoid mixing concepts

4. **Follow Conventions**
   - Match existing style
   - Use consistent naming
   - Maintain structure

## Common Issues

**Q: My notebook has errors when running?**
A: Debug locally, test all cells work in order

**Q: How do I reference external files?**
A: Use relative paths from repo root

**Q: Can I use a different package version?**
A: Update requirements.txt and note compatibility

## Getting Help

- Check existing notebooks for examples
- Review [CONTRIBUTING.md](CONTRIBUTING.md)
- Open an issue for questions

## Resources

- [Jupyter Best Practices](https://jupyter-notebook.readthedocs.io/)
- [LangChain Docs](https://python.langchain.com/)
- [LangGraph Docs](https://langchain-ai.github.io/langgraph/)

## Licensing

By contributing, you agree your work is licensed under MIT License.

---

Thank you for contributing! 🎉
