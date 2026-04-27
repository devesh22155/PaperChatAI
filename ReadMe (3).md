# PaperChatAI-RAG

An AI-powered chatbot that allows you to interact with your PDF documents using Retrieval-Augmented Generation (RAG). Upload your PDFs and ask questions — the system will generate accurate answers strictly based on the document content.

---

## Features

- Upload single or multiple PDF files  
- Automatic text extraction from PDFs  
- Smart text chunking for large documents  
- Embedding generation using Google Generative AI  
- Fast similarity search with FAISS  
- Context-aware answers using Gemini-Pro  
- Answers restricted to provided context  
- Simple and interactive Streamlit UI  

---

## How It Works

This project implements a RAG (Retrieval-Augmented Generation) pipeline:

1. Extract text from uploaded PDFs  
2. Split text into manageable chunks  
3. Convert chunks into embeddings  
4. Store embeddings in a FAISS vector database  
5. When a user asks a question:
   - Retrieve relevant chunks
   - Pass them to the LLM (Gemini-Pro)
   - Generate a context-based answer  

---

## Tech Stack

- Frontend/UI: Streamlit  
- LLM: Google Gemini-Pro  
- Embeddings: Google Generative AI Embeddings  
- Vector DB: FAISS  
- Framework: LangChain  
- PDF Processing: PyPDF2  

---

## Project Structure

```
.
├── app.py                 # Main Streamlit app
├── faiss_index/          # Saved vector database
├── .env                  # API keys (not included in repo)
├── requirements.txt      # Dependencies
└── README.md             # Project documentation
```

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ChatWithPDF-RAG.git
cd ChatWithPDF-RAG
```

---

### 2. Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate     # Mac/Linux
venv\Scripts\activate        # Windows
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Set Up Environment Variables

Create a `.env` file in the root directory:

```
GOOGLE_API_KEY=your_api_key_here
```

---

### 5. Run the Application

```bash
streamlit run app.py
```

---

## Usage

1. Upload your PDF(s) from the sidebar  
2. Click Process to generate embeddings  
3. Ask any question related to the document  
4. Get accurate, context-based answers  

---

## Limitations

- Answers are limited to the uploaded document content  
- Large PDFs may take time to process  
- No chat history (stateless interactions)  
- FAISS index is stored locally  

---

## Future Improvements

- Add conversational memory (chat history)  
- Support for multiple document formats (DOCX, TXT)  
- Deploy as a web app (AWS / GCP / Vercel)  
- Improve UI/UX  
- Add document highlighting for answers  

---

## Contributing

Contributions are welcome. Feel free to fork the repository and submit a pull request.

---

## License

This project is licensed under the MIT License.

---

## Acknowledgements

- LangChain  
- Google Generative AI  
- FAISS  
- Streamlit  

---

## Support

If you find this project useful, consider giving it a star on GitHub.
