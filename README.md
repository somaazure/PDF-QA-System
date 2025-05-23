# PDF-QA-System
PDF-QA-System


Here’s a well-structured **GitHub README-style description** of your **PDF Question Answering System**, with bullet points explaining the core functionalities. I've also integrated the screenshot you shared to visually support the description.

---

# 📄 PDF Question Answering System

> Upload any PDF document and ask questions about its content — including **text, images, and tables** — powered by LangChain, OpenAI, and Gradio.

![App Screenshot](attachment:/mnt/data/ff1b980a-3adf-4c09-96e6-68ce6eb10c07.png)

---

## 🚀 Core Features

* ✅ **PDF Parsing & Chunking**: Extracts and splits PDF text into manageable chunks using `PyPDF2` and LangChain’s `CharacterTextSplitter`.
* 🧠 **Retrieval-Augmented Generation (RAG)**: Combines document retrieval with LLM-based answering for high relevance.
* 🔍 **Query Expansion**: Automatically expands user queries using LLMs to improve retrieval effectiveness.
* 🖼️ **Image & Table Extraction**: Uses `PyMuPDF` and `pytesseract` to extract embedded images and tabular data from the PDF.
* 🗃️ **Vector Embeddings**: Creates FAISS-based vectorstore using OpenAI Embeddings for similarity search.
* 🔧 **Gradio UI**: Easy-to-use web interface allowing PDF upload and natural language querying.

---

## 🛠️ Stack Overview

| Component    | Technology           |
| ------------ | -------------------- |
| LLM          | OpenAI GPT-4o-mini   |
| Embeddings   | OpenAI Embeddings    |
| Vector Store | FAISS                |
| PDF Parsing  | PyPDF2, PyMuPDF      |
| OCR & Tables | Pytesseract, pandas  |
| UI           | Gradio               |
| Environment  | Python + .env config |

---

## 🔁 Workflow

1. **User uploads a PDF**
2. **Text is split** into chunks (1000 tokens with 100 overlap)
3. **Vector embeddings** are created and stored in FAISS
4. **Query expansion** enhances retrieval accuracy
5. **Relevant chunks** are passed with images/tables info to GPT model
6. **Answer is generated**, along with a log of the retrieval process

---

## 💡 Sample Use Case

> Upload a BDA Development Plan PDF and ask:
> *"What’s the documents checklist, summarize in 10 lines?"*

Output: A list of key documents, retrieved and summarized based on the PDF contents.
(Screenshot above shows a working example.)

---

## 📂 Folder Structure Suggestion

```
pdf-qa-system/
│
├── main.py                # Full app code
├── .env                   # Your OpenAI API key
├── requirements.txt       # Python dependencies
├── README.md              # This description
└── assets/
    └── app-screenshot.png # UI screenshot
```

---

## 📦 Requirements

Install with:

```bash
pip install -r requirements.txt
```

---

## ✅ Sample `.env` File

```env
OPENAI_API_KEY=your_openai_api_key
```


![image](https://github.com/user-attachments/assets/59bfcaf6-2db5-425f-9221-2b1fc44883e6)

