# 📄 Chat with Multiple PDFs - Streamlit App

A powerful Streamlit application that enables users to upload multiple PDF files and ask context-aware questions. It leverages **LangChain** and **Google's Gemini API** to provide intelligent responses based on PDF content.

✨ Features
✅ PDF Upload: Upload multiple PDF files for processing.
💬 Question Answering: Ask questions related to the content of the uploaded PDFs.
📚 Contextual Responses: Utilizes LangChain and Gemini API for accurate answers.
📝 Conversation History: Keeps track of previous questions and answers.
📥 Download Conversation: Export the chat history as a CSV file.
🔄 Reset & Rerun: Reset the application or rerun the last query.
🔗 Google Gemini Integration: Uses Gemini API for embeddings and Q&A.
🎨 User-Friendly Interface: Simple and intuitive Streamlit UI.

yaml
Copy
Edit

---

🚀 Live Demo
🌍 Try it out now: Chat with PDFs

yaml
Copy
Edit

---

🔧 Prerequisites
Ensure you have the following installed:

Python 3.7+

Streamlit

PyPDF2

Pandas

LangChain

Google Generative AI (Gemini) API Key

yaml
Copy
Edit

---

🛠 Installation
1️⃣ Clone the Repository

bash
Copy
Edit
git clone <repository_url>
cd <repository_directory>
2️⃣ Install Dependencies

bash
Copy
Edit
pip install streamlit PyPDF2 pandas langchain langchain-google-genai faiss-cpu
3️⃣ Obtain a Google Gemini API Key

Visit Google AI Studio

Create a project and generate an API key.

yaml
Copy
Edit

---

🚀 How to Run
1️⃣ Save the Python script
Save the application code as pdf_chat.py.

2️⃣ Run the Streamlit app

bash
Copy
Edit
streamlit run pdf_chat.py
3️⃣ Interact with the Application

Upload PDFs, enter the API key, and start asking questions!

yaml
Copy
Edit

---

🎯 Usage Guide
🔑 Enter API Key

Enter your Google Gemini API key in the sidebar.

📂 Upload PDF Files

Click "Browse files" and upload one or more PDFs.

Click "Submit & Process."

❓ Ask Questions

Type a question in the input field and press Enter.

📖 View Answers & History

The application displays responses and stores conversation history.

📥 Download Chat History

Click "Download conversation history as CSV" in the sidebar.

🔄 Reset or Rerun

Use the reset and rerun buttons in the sidebar.

yaml
Copy
Edit

---

📝 Code Overview
🔍 Core Functions:

get_pdf_text(pdf_docs): Extracts text from uploaded PDFs.

get_text_chunks(text, model_name): Splits extracted text into smaller chunks.

get_vector_store(text_chunks, model_name, api_key): Creates a FAISS vector store.

get_conversational_chain(model_name, vectorstore, api_key): Sets up the Q&A system.

user_input(user_question, model_name, api_key, pdf_docs, conversation_history): Processes user queries.

main(): Handles the Streamlit UI and user interactions.

yaml
Copy
Edit

---

📦 Dependencies
Streamlit - For the web interface

PyPDF2 - For extracting text from PDFs

Pandas - For managing data

LangChain - For handling AI-based responses

Langchain Google Genai - For Gemini API integration

FAISS - For efficient text search

yaml
Copy
Edit

---

🔔 Notes
✔ Ensure you have a valid Google Gemini API key.
✔ FAISS stores vectors locally in the faiss_index directory.
✔ Handles multiple PDF uploads.
✔ Includes error handling for smooth user experience.
✔ Custom CSS styles the chat interface.
✔ Supports downloading conversation history.

yaml
Copy
Edit

---

💖 Made with Love
❤️ Made with love by Nilesh Mete

yaml
Copy
Edit

---

🚀 Start chatting with your PDFs today!

Copy
Edit
