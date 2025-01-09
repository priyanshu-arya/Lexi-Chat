# Lexi-Chat Enterprise Document Intelligence System

# Chat With Documents 📚

An intelligent document management and chat system powered by OpenAI's GPT-4 and vector embeddings. This application allows users to upload PDF documents, automatically extract key information, organize documents with tags, and have interactive conversations with their document content using natural language.

## 🌟 Features

- **PDF Document Processing**: Upload and process PDF documents with automatic fact extraction
- **Smart Tagging System**: Automatic tag suggestions and management for better document organization
- **Vector Search**: Utilizes pgvector for efficient similarity search in document contents
- **Interactive Chat Interface**: Natural language conversations with document content using GPT-4
- **Reference Tracking**: View source references for chat responses
- **Modern UI**: Built with Streamlit for a clean, responsive interface

## 🚀 Technology Stack

- **Python 3.x**
- **Streamlit**: For the web interface
- **PostgreSQL with pgvector**: For document storage and vector similarity search
- **OpenAI API**: For GPT-4 integration and text embeddings
- **Peewee ORM**: For database operations
- **pdftotext**: For PDF text extraction

## 📋 Prerequisites

- Python 3.x
- PostgreSQL with pgvector extension installed
- OpenAI API key
- PostgreSQL database

## 💻 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/chat-with-documents.git
cd chat-with-documents
```

2. Install required Python packages:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root with the following configurations:
```env
POSTGRES_DB_NAME=your_db_name
POSTGRES_DB_HOST=your_db_host
POSTGRES_DB_PORT=your_db_port
POSTGRES_DB_USER=your_db_user
POSTGRES_DB_PASSWORD=your_db_password
OPENAI_API_KEY=your_openai_api_key
```

4. Set up PostgreSQL with pgvector:
```sql
CREATE EXTENSION vector;
CREATE EXTENSION ai;
```

5. Run the application:
```bash
streamlit run "Chat With Documents.py"
```

## 🗂️ Project Structure

- `Chat With Documents.py`: Main chat interface
- `Manage Documents.py`: Document upload and management interface
- `Manage Tags.py`: Tag management system
- `constants.py`: System prompts and constants
- `db.py`: Database models and configuration
- `utils.py`: Utility functions
- `env.py`: Environment configuration

## 📖 Usage

1. **Managing Tags**:
   - Navigate to the Tags management page
   - Create tags for document organization
   - Delete unused tags

2. **Uploading Documents**:
   - Go to the Document management page
   - Upload PDF documents
   - System automatically extracts facts and suggests tags
   - View and manage uploaded documents

3. **Chatting with Documents**:
   - Use the main Chat interface
   - Ask questions about your documents
   - View source references for answers
   - Get AI-powered responses based on document content

## 🔍 How It Works

1. **Document Processing**:
   - Documents are chunked into optimal sizes
   - Facts are extracted using GPT-4
   - Text is converted to embeddings using OpenAI's embedding model
   - Tags are automatically suggested based on content

2. **Chat System**:
   - User queries are converted to embeddings
   - Similar document chunks are retrieved using vector similarity
   - GPT-4 generates responses based on relevant document content
   - Source references are provided for transparency

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⚠️ Important Notes

- Ensure your OpenAI API key has sufficient credits
- Large PDF files may take longer to process
- The system works best with text-based PDFs
- Configure PostgreSQL with adequate resources for vector operations

## 🔮 Future Enhancements

- Support for more document formats
- Advanced search capabilities
- Custom embedding models
- Batch document processing
- Enhanced tag suggestions
- Document version control

## 💡 Keywords
document management, chatbot, OpenAI, GPT-4, vector search, PDF processing, natural language processing, document chat, AI-powered search, document analysis, text embeddings, PostgreSQL, pgvector, Python, Streamlit
