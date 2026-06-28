# 📄 RAG-Based PDF Semantic Search (MongoDB + OpenAI)

A **Retrieval-Augmented Generation (RAG)** system that enables semantic search over PDF documents using **vector embeddings** and **MongoDB Atlas Vector Search**.

This project allows users to ask natural language questions and retrieve the most relevant content from a PDF.

---

## 🚀 Features

- 📥 Load and process PDF documents  
- ✂️ Intelligent text chunking using LangChain  
- 🧠 Generate embeddings using OpenAI-compatible API  
- 🗄️ Store vectors in MongoDB Atlas  
- 🔍 Perform fast semantic search using vector similarity  
- ⚡ Retrieve top-k relevant document chunks  
- 🔁 Reusable query function for dynamic searches  

---

## 🏗️ Tech Stack

- Python  
- MongoDB Atlas (Vector Search)  
- OpenAI Embeddings API (via OpenRouter)  
- LangChain (PDF Loader + Text Splitter)  
- PyMongo  
- Jupyter Notebook  

---

## 📊 Architecture


PDF → Text Splitting → Embeddings → MongoDB Atlas
↓
User Query → Embedding → Vector Search → Relevant Results


---

## 📁 Project Structure


├── test.ipynb # Main notebook with full pipeline
├── file.pdf # Input document
├── README.md # Project documentation


---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/rag-pdf-search.git
cd rag-pdf-search
2. Install Dependencies
pip install pymongo langchain openai python-dotenv
3. Set Environment Variables

Create a .env file:

OPENAI_API_KEY=your_api_key_here
MONGO_URI=your_mongodb_connection_string
4. Run the Project

Open and execute:

test.ipynb
🧠 How It Works
Step 1: Load PDF
Uses LangChain’s PDF loader to extract text
Step 2: Split Text
Breaks document into smaller chunks for better embedding quality
Step 3: Generate Embeddings
Converts text into high-dimensional vectors
Step 4: Store in MongoDB
Each chunk + embedding stored as a document
Step 5: Vector Search
User query is embedded and compared using cosine similarity
🔍 Example Usage
get_query_results("What is MongoDB?")
Output

Returns the most relevant text chunks from the PDF based on semantic similarity.

⚠️ Important Notes
Ensure embedding field name matches index (embedding)
MongoDB vector index must be created before querying
Do NOT expose API keys in code
Use .env for secure configuration
🐞 Known Issues / Fixes
❌ Issue
collection.searchable_docs.aggregate(...)
✅ Fix
collection.aggregate(...)
❌ Issue
"embeddings"
✅ Fix
"embedding"
📈 Future Improvements
🤖 Add LLM response generation (ChatGPT-style answers)
🌐 Build a frontend (React / Next.js)
📊 Add reranking for better accuracy
🔐 Authentication & user-based document storage
☁️ Deploy using Render / Vercel / AWS
💼 Use Cases
Document search systems
Knowledge base assistants
Research paper querying
Internal company search tools
🏷️ GitHub Topics (Add These)
rag
semantic-search
mongodb
vector-database
openai
langchain
machine-learning
nlp
python
ai-project
🙌 Author

Mohamed Nusaif

💻 Full Stack Developer
📊 Aspiring Ai Developer
⭐ Support

If you like this project:

⭐ Star the repo
🍴 Fork it
📢 Share it
