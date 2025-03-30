# 📄 Chat with Multiple PDFs - Streamlit App

A powerful Streamlit application that allows users to upload multiple PDF files and ask context-aware questions. This app leverages **LangChain** and **Google's Gemini API** to provide intelligent responses based on the content of uploaded PDFs.

---

## ✨ Features
✅ **Upload Multiple PDFs** - Easily upload and process multiple PDF documents.  
💬 **Intelligent Q&A** - Ask questions related to the content of uploaded PDFs.  
📚 **Context-Aware Responses** - Utilizes LangChain and Gemini API for precise answers.  
📝 **Conversation History** - Tracks previous interactions for easy reference.  
📥 **Export Chat History** - Download conversation logs as a CSV file.  
🔄 **Reset & Rerun** - Reset the application or rerun the last query effortlessly.  
🔗 **Google Gemini Integration** - Uses Gemini API for embeddings and Q&A.  
🎨 **User-Friendly Interface** - A simple, intuitive, and efficient UI.  

---

## 🚀 Live Demo
🌍 **Try it now:** [bvimitbot.streamlit.app](bvimitbot.streamlit.app)  
🔗 **Deployed on:** Streamlit Cloud  
👨‍💼 **Created by:** [Nilesh Mete](https://www.linkedin.com/in/nileshmete993088/)  

---

## 🔧 Prerequisites
Ensure you have the following installed:
- Python 3.7+
- Streamlit
- PyPDF2
- Pandas
- LangChain
- Google Generative AI (Gemini) API Key

---

## 🛠 Installation Guide
### 1️⃣ Clone the Repository
```bash
git clone <repository_url>
cd <repository_directory>
```
### 2️⃣ Install Dependencies
```bash
pip install streamlit PyPDF2 pandas langchain langchain-google-genai faiss-cpu
```
### 3️⃣ Obtain Google Gemini API Key
- Visit **Google AI Studio**
- Create a project and generate an API key

---

## 🚀 How to Run
### 1️⃣ Save the Python Script
Save the application code as **pdf_chat.py**.

### 2️⃣ Start the Streamlit App
```bash
streamlit run pdf_chat.py
```

### 3️⃣ Interact with the Application
- Upload PDFs
- Enter your API key
- Start asking questions!

---

## 🎯 Usage Guide
### 🔑 Enter API Key
Enter your **Google Gemini API key** in the sidebar.

### 📂 Upload PDF Files
- Click "Browse files" and upload one or more PDFs.
- Click "Submit & Process" to analyze the documents.

### ❓ Ask Questions
- Type a question in the input field and press **Enter**.
- Receive AI-generated responses based on PDF content.

### 📖 View Answers & History
- The app maintains a record of your questions and responses.

### 📥 Download Chat History
- Click "Download conversation history as CSV" in the sidebar.

### 🔄 Reset or Rerun
- Use the **reset** and **rerun** buttons for fresh interactions.

---

## 📝 Code Overview
### 🔍 Core Functions:
- **get_pdf_text(pdf_docs)** - Extracts text from uploaded PDFs.
- **get_text_chunks(text, model_name)** - Splits extracted text into smaller chunks.
- **get_vector_store(text_chunks, model_name, api_key)** - Creates a FAISS vector store.
- **get_conversational_chain(model_name, vectorstore, api_key)** - Sets up the Q&A system.
- **user_input(user_question, model_name, api_key, pdf_docs, conversation_history)** - Processes user queries.
- **main()** - Manages the Streamlit UI and user interactions.

---

## 📦 Dependencies
- **Streamlit** - Web-based UI framework.
- **PyPDF2** - Extracts text from PDFs.
- **Pandas** - Manages data structures.
- **LangChain** - AI-powered question-answering framework.
- **LangChain Google GenAI** - Integrates with Gemini API.
- **FAISS** - Efficient text search and retrieval.

---

## 🔔 Notes
✔ Ensure you have a **valid Google Gemini API key**.  
✔ FAISS stores vectors locally in the **faiss_index directory**.  
✔ Supports **multiple PDF uploads**.  
✔ Includes **robust error handling** for smooth user experience.  
✔ Custom **CSS for an enhanced chat interface**.  
✔ **Downloadable chat history** for easy reference.  

---

## 💖 Made with Love
❤️ Created by [Nilesh Mete](https://www.linkedin.com/in/nileshmete993088/)  

🚀 **Start chatting with your PDFs today!**

