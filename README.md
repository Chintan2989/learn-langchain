# 📚 LangChain PDF Q&A System

A comprehensive collection of Jupyter notebooks for PDF processing, vector database creation, and intelligent question-answering using LangChain and Google's Gemini AI.

## 🎯 Overview

This project provides two main workflows:
- **Comprehensive PDF Workflow** (`langchain_pdf_workflow.ipynb`) - Full pipeline for PDF processing, updating, and regeneration
- **Simple PDF Q&A** (`read_pdf.ipynb`) - Streamlined document analysis and question-answering system

## 🚀 Features

### ✨ Core Capabilities
- 📖 **PDF Loading**: Extract text from PDF documents
- 🧠 **Smart Chunking**: Intelligent text segmentation for better search results
- 🔍 **Vector Search**: FAISS-powered similarity search
- 🤖 **AI Q&A**: Google Gemini 2.0 Flash for natural language responses
- 💾 **Database Persistence**: Save and load vector databases
- 🎯 **Car-Specific Processing**: Optimized for automotive inventory documents

### 🔧 Technical Stack
- **LangChain Community**: PDF processing and text splitting
- **Google Gemini 2.0 Flash**: Embeddings and text generation
- **FAISS**: Vector similarity search
- **PyPDF**: PDF document loading
- **Python-dotenv**: Environment management

## 📋 Quick Start

### 1. Setup Environment

```bash
# Install required packages
pip install langchain-community langchain-google-genai faiss-cpu pypdf python-dotenv google-generativeai
```

### 2. Configure API Key

Create a `.env` file in the project directory:
```env
GOOGLE_API_KEY=your-google-ai-api-key-here
```

Get your API key from: [Google AI Studio](https://aistudio.google.com/app/apikey)

### 3. Choose Your Workflow

#### 🎯 Simple Q&A (Recommended for Beginners)
Open `read_pdf.ipynb` for a streamlined experience:
- Load any PDF document
- Ask questions in natural language
- Get AI-powered answers

#### 🔧 Comprehensive Workflow
Open `langchain_pdf_workflow.ipynb` for advanced features:
- Full PDF processing pipeline
- Content updating capabilities
- PDF regeneration

## 📖 File Descriptions

### 📓 `read_pdf.ipynb` - Simple PDF Q&A
**Perfect for quick document analysis and Q&A**

#### Key Features:
- **Smart PDF Loading**: Automatic text extraction and preprocessing
- **Car-Specific Chunking**: Optimized for automotive inventory documents
- **Intelligent Search**: Vector-based similarity search with debugging
- **Natural Q&A**: Ask questions in plain English
- **Persistent Storage**: Save and reload vector databases

#### Workflow:
1. **Load PDF** → 2. **Create Vector DB** → 3. **Search/Ask Questions**

#### Example Usage:
```python
# Load your PDF
pdf_db.load_pdf("your_document.pdf")
pdf_db.create_vector_database()

# Search for specific content
results = pdf_db.search("BMW", k=2)

# Ask questions
answer = pdf_db.answer_question("What is the price of Honda Civic?")
```

### 📓 `langchain_pdf_workflow.ipynb` - Comprehensive Workflow
**Advanced PDF processing with update capabilities**

#### Key Features:
- **Full Pipeline**: Complete PDF → Vector DB → Update → New PDF workflow
- **Content Updates**: Modify and update document content
- **PDF Generation**: Create new PDFs with updated information
- **Demonstration Data**: Built-in sample PDF creation

## 🏗️ Project Structure

```
learn-langchain/
├── README.md                           # This file
├── read_pdf.ipynb                      # Simple PDF Q&A notebook
├── langchain_pdf_workflow.ipynb        # Comprehensive workflow
├── .env                                # API keys (create this)
├── carData.pdf                         # Sample PDF data
├── pdf_vector_db/                      # Vector database storage
│   ├── index.faiss
│   └── index.pkl
└── DOCS.md                             # Detailed documentation
```

## 🎯 Use Cases

### 📄 Document Analysis
- Research paper analysis
- Legal document review
- Technical manual exploration
- Academic literature review

### 🚗 Automotive Industry
- Car inventory management
- Vehicle specification lookup
- Pricing and feature comparison
- Maintenance record analysis

### 📊 Business Intelligence
- Report analysis
- Data extraction from PDFs
- Content summarization
- Information retrieval

## 🔍 Search Capabilities

### Smart Chunking Strategies
1. **Car-Specific Chunking**: Separates individual vehicle information
2. **Brand Detection**: Identifies automotive brands and models
3. **Metadata Enrichment**: Adds contextual information to chunks
4. **Fallback Mechanisms**: Traditional text splitting when needed

### Search Features
- **Similarity Scoring**: Shows relevance scores for results
- **Debug Information**: Detailed search diagnostics
- **Multiple Results**: Configurable number of results
- **Query Analysis**: Direct vs semantic matching detection

## 🚀 Getting Started Examples

### Basic PDF Q&A
```python
# Initialize the system
pdf_db = PDFVectorDB()

# Load your document
pdf_db.load_pdf("your_document.pdf")
pdf_db.create_vector_database()

# Start asking questions!
pdf_db.answer_question("What are the main topics in this document?")
```

### Advanced Search
```python
# Search with debugging
results = pdf_db.search("specific topic", k=3)

# Check database status
pdf_db.get_status()

# Load existing database
pdf_db.load_existing_database("saved_db_path")
```

## 🔧 Troubleshooting

### Common Issues

#### ❌ "No vector database found"
**Solution**: Run `pdf_db.create_vector_database()` after loading a PDF

#### ❌ "GOOGLE_API_KEY not found"
**Solution**: Create `.env` file with your Google AI API key

#### ❌ "Poor search results"
**Solution**: Try the database reset cell to improve chunking

#### ❌ "PDF not loading"
**Solution**: Check file path and ensure PDF is not corrupted

### Debug Tips
- Use `pdf_db.get_status()` to check system state
- Enable debug mode in search for detailed information
- Try different chunk sizes for different document types

## 🔮 Advanced Features

### Custom Chunking
Modify the `_create_car_specific_chunks()` method to handle different document types.

### Multiple PDFs
Load and process multiple documents in sequence.

### Database Management
Save, load, and manage multiple vector databases for different projects.

## 🤝 Contributing

Feel free to submit issues, feature requests, or pull requests to improve the system!

## 📝 License

This project is open source and available under the MIT License.

---

**Happy Document Analysis! 🎉**

For detailed technical documentation, see `DOCS.md`
# learn-langchain
# learn-langchain
