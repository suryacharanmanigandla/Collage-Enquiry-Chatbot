# BVRIT College Enquiry Chatbot

An AI-powered chatbot that answers questions about BVRIT (B V Raju Institute of Technology) using **Retrieval-Augmented Generation (RAG)**.

The chatbot scrapes college website content, converts it into vector embeddings, stores them in a FAISS vector database, and uses Google Gemini LLM to generate intelligent responses.

---

## Architecture

```
User → Chatbot UI → Node.js Server → Python FastAPI Backend
                                        ├── Vector Search (FAISS)
                                        └── LLM Response (Gemini)
```

## Project Structure

```
college-chatbot/
├── scraper/                    # Web scraping module
│   └── scrape_college_data.py
# BVRIT College Enquiry Chatbot

An AI-powered college enquiry chatbot for BVRIT (B V Raju Institute of Technology) built with a Retrieval-Augmented Generation (RAG) pipeline.

The system scrapes official college content, processes it into text chunks, generates embeddings, stores them in a FAISS vector database, and uses a Groq-hosted Llama model to answer user questions from retrieved context.

## Features

- RAG-based question answering from BVRIT website content
- FastAPI backend for chat and search endpoints
- Express server for serving the frontend
- Responsive chat UI with quick-question shortcuts
- Vector search over scraped and embedded college data


```text
User -> Frontend (HTML/CSS/JS) -> FastAPI API -> FAISS Vector DB -> Groq LLM -> Answer
```

## Tech Stack
- **Python:** FastAPI, Uvicorn
- **Retrieval:** Sentence Transformers, FAISS
- **LLM:** Groq API with Llama models
- **Scraping:** Requests, BeautifulSoup
├── backend/
│   ├── api.py
│   └── server.js
├── frontend/
│   ├── index.html
├── vector_db/
├── data/
├── run_pipeline.py
├── requirements.txt
└── package.json
```

## Prerequisites

- Python 3.10+
- Node.js 18+
- A Groq API key

## Setup

### 1. Open the project folder

```powershell
cd c:\Users\obban\OneDrive\Desktop\chatbot
```

.venv\Scripts\Activate.ps1
```

### 3. Install Python dependencies

```powershell
pip install -r requirements.txt
```

### 4. Install Node.js dependencies

```powershell
npm install
```

### 5. Configure environment variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
```

## Build the Vector Database

Run the pipeline once to scrape the website, clean the text, generate embeddings, and build the FAISS index:

```powershell
python run_pipeline.py
```

You can skip this step if `vector_db/faiss_index.bin` and `vector_db/chunks_metadata.pkl` already exist.

## Run the Application

### Terminal 1: Start the Python API

```powershell
cd backend
python api.py
```

The API runs at `http://127.0.0.1:5000`.

### Terminal 2: Start the Node.js server


http://localhost:3000

- `GET /` — health check
 # BVRIT College Enquiry Chatbot
 
 AI-powered chatbot for answering BVRIT (B V Raju Institute of Technology) enquiry questions using a Retrieval-Augmented Generation (RAG) pipeline.
 
 Repository: https://github.com/Mukesh-1729/CollegeChatbot.git
 
 ## Overview
 
 This project:
 
 - scrapes official BVRIT website content
 - cleans and chunks the data
 - generates embeddings
 - stores them in a FAISS vector database
 - uses a Groq-hosted Llama model to generate answers from retrieved context
 
 ## Features
 
 - RAG-based question answering
 - FastAPI backend for chat and search endpoints
 - Express server for serving the frontend
 - Responsive chat UI with quick questions
 - Source-aware responses from college content
 
 ## Architecture
 
 ```text
 User -> Frontend (HTML/CSS/JS) -> FastAPI API -> FAISS Vector DB -> Groq LLM -> Answer
 ```
 
 ## Tech Stack
 
 - **Frontend:** HTML, CSS, JavaScript
 - **Node.js:** Express, http-proxy-middleware
 - **Python:** FastAPI, Uvicorn
 - **Retrieval:** Sentence Transformers, FAISS
 - **LLM:** Groq API with Llama models
 - **Scraping:** Requests, BeautifulSoup
 
 ## Project Structure
 
 ```text
 chatbot/
 ├── backend/
 │   ├── api.py
 │   └── server.js
 ├── frontend/
 │   ├── index.html
 │   ├── script.js
 │   └── style.css
 ├── scraper/
 ├── processing/
 ├── embeddings/
 ├── llm/
 ├── vector_db/
 ├── data/
 ├── run_pipeline.py
 ├── requirements.txt
 └── package.json
 ```
 
 ## Prerequisites
 
 - Python 3.10+
 - Node.js 18+
 - A Groq API key
 
 ## Setup
 
 ### 1. Clone or open the project
 
 ```powershell
 cd c:\Users\obban\OneDrive\Desktop\chatbot
 ```
 
 ### 2. Activate the Python virtual environment
 
 ```powershell
 .venv\Scripts\Activate.ps1
 ```
 
 ### 3. Install Python dependencies
 
 ```powershell
 pip install -r requirements.txt
 ```
 
 ### 4. Install Node.js dependencies
 
 ```powershell
 npm install
 ```
 
 ### 5. Create the `.env` file
 
 Create a `.env` file in the project root and add your Groq key:
 
 ```env
 GROQ_API_KEY=your_groq_api_key_here
 ```
 
 ## Build the Vector Database
 
 Run the pipeline once to scrape, process, embed, and build the FAISS index:
 
 ```powershell
 python run_pipeline.py
 ```
 
 You can skip this step if `vector_db/faiss_index.bin` and `vector_db/chunks_metadata.pkl` already exist.
 
 ## Run the Application
 
 ### Terminal 1: Start the Python API
 
 ```powershell
 cd backend
 python api.py
 ```
 
 The API runs at:
 
 ```text
 http://127.0.0.1:5000
 ```
 
 ### Terminal 2: Start the Node.js server
 
 ```powershell
 cd c:\Users\obban\OneDrive\Desktop\chatbot
 npm start
 ```
 
 The frontend runs at:
 
 ```text
 http://localhost:3000
 ```
 
 ## API Endpoints
 
 - `GET /` — health check
 - `GET /health` — detailed status
 - `POST /chat` — generate a RAG answer
 - `POST /search` — return similar chunks only
 
 ## Example Questions
 
 - What is BVRIT?
 - What is the admission process?
 - What are the placement statistics?
 - What departments are available?
 - What is the fee structure?
 
 ## Troubleshooting
 
 - **Backend offline:** start `python api.py` in the `backend` folder.
 - **Vector DB missing:** run `python run_pipeline.py`.
 - **API key error:** verify `GROQ_API_KEY` in `.env`.
 - **Frontend cannot connect:** make sure both backend and frontend servers are running.
 
 ## License
 
 MIT
- `GET /health` — detailed status
- `POST /chat` — generate a RAG answer
- `POST /search` — return similar chunks only

## Example Questions

- What is BVRIT?
- What is the admission process?
- What are the placement statistics?
- What departments are available?
- What is the fee structure?

## Notes

- The frontend connects directly to the FastAPI backend at `http://localhost:5000`.
- If the backend is offline, the UI will show a connection error.
- If the vector database is missing, rerun `python run_pipeline.py`.

## License

MIT# Collage-Enquiry-Chatbot
