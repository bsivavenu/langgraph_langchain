# Data Ingestion & Parsing

Comprehensive guide to loading, parsing, and preparing data for LLM applications.

## 📁 Folder Contents

This folder contains 6 detailed notebooks covering different data sources:

### 1. **1-dataingestion.ipynb**
Basic data ingestion concepts:
- Loading data from various sources
- Data format recognition
- Preprocessing approaches
- Best practices for data pipelines

### 2. **2-dataparsingpdf.ipynb**
PDF document processing:
- Extract text from PDFs
- Handle multi-page documents
- Preserve formatting and structure
- Deal with scanned PDFs (OCR)

### 3. **3-dataparsingdoc.ipynb**
Word document processing:
- Parse .docx files
- Extract sections and headings
- Handle tables and images
- Preserve document structure

### 4. **4-csvexcelparsing.ipynb**
Spreadsheet data handling:
- Load CSV files
- Parse Excel workbooks
- Handle multiple sheets
- Data type inference and cleaning

### 5. **5-jsonparsing.ipynb**
JSON and structured data:
- Parse JSON documents
- Handle nested structures
- Work with APIs
- Data validation

### 6. **6-databaseparsing.ipynb**
Database integration:
- Connect to databases
- Query and extract data
- Stream large datasets
- Data transformation

## 🚀 Quick Start

### Setup
```bash
cd 0-DataIngestParsing
jupyter notebook
```

### Example: Load a PDF

```python
from langchain.document_loaders import PyPDFLoader

loader = PyPDFLoader("path/to/document.pdf")
documents = loader.load()

for doc in documents:
    print(doc.page_content[:100])
    print(doc.metadata)
```

### Example: Load CSV

```python
import pandas as pd

df = pd.read_csv("data.csv")
print(df.head())
print(df.info())
```

## 📊 Data Formats Covered

| Format | Notebook | Tools |
|--------|----------|-------|
| **PDF** | 2-dataparsingpdf.ipynb | PyPDF, pdfplumber |
| **DOCX** | 3-dataparsingdoc.ipynb | python-docx, docx2txt |
| **CSV/Excel** | 4-csvexcelparsing.ipynb | Pandas, openpyxl |
| **JSON** | 5-jsonparsing.ipynb | json, pandas |
| **Database** | 6-databaseparsing.ipynb | SQLAlchemy |

## 🔄 Data Pipeline Workflow

```
Raw Data
   ↓
Load (Read from source)
   ↓
Parse (Extract structure)
   ↓
Clean (Remove noise)
   ↓
Transform (Format for LLM)
   ↓
Chunk (Split into sections)
   ↓
Embed (Create vectors)
   ↓
Store (Save for retrieval)
```

## 📁 Data Folder

Sample data files are in the `data/` subfolder:
- Sample PDFs
- Sample Excel files
- Sample JSON files
- Sample CSV files

Use these for practice and testing.

## 💡 Key Concepts

### Document Loaders
Tools for loading different document types into LangChain format.

### Chunking
Breaking documents into manageable pieces for processing.

### Metadata
Preserving document metadata (source, author, date, etc.)

### Batch Processing
Handling large document collections efficiently.

## 🔗 Integration with RAG

After preparing data here, use it in:
- Embedding notebooks for vectorization
- RAG notebooks for retrieval-augmented generation
- Agent notebooks for document-based reasoning

## 📝 Best Practices

1. **Data Validation** - Check data integrity after loading
2. **Error Handling** - Handle corrupted or malformed files
3. **Metadata Preservation** - Keep source information
4. **Batch Processing** - Use chunks for large datasets
5. **Testing** - Test with sample data first

## 🚨 Common Issues

**Q: PDF text extraction gives garbled output?**
A: PDF may be scanned. Use OCR or try different loader.

**Q: Excel formulas aren't preserved?**
A: Extract values, not formulas. Use `data_only=True` in openpyxl.

**Q: Large file causes memory issues?**
A: Process in chunks or use streaming approaches.

## 🔗 Related Topics

- See `1-densesparse.ipynb` for retrieval after ingestion
- See `1-semantichunking.ipynb` for intelligent chunking
- See `embedding.ipynb` for vectorization

---

**Created:** February 2, 2026  
**Status:** ✅ Complete
