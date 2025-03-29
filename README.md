# Chat with Multiple PDFs Streamlit App


This Streamlit application allows users to upload multiple PDF files and ask questions about their content. It leverages LangChain and Google's Gemini API to provide intelligent and context-aware answers.

## Features

-   **PDF Upload:** Users can upload multiple PDF files for processing.
-   **Question Answering:** Users can ask questions related to the content of the uploaded PDFs.
-   **Contextual Responses:** The application uses LangChain and Gemini to provide answers based on the context of the PDFs.
-   **Conversation History:** The application maintains a conversation history, displaying previous questions and answers.
-   **Download Conversation:** Users can download the conversation history as a CSV file.
-   **Reset and Rerun:** Users can reset the application or rerun the last query.
-   **Google Gemini Integration:** Uses Google's Gemini API for embeddings and question answering.
-   **User-Friendly Interface:** Provides a clean and intuitive Streamlit interface.

## Prerequisites

-   Python 3.7+
-   Streamlit
-   PyPDF2
-   Pandas
-   LangChain
-   Google Generative AI (Gemini) API key

## Installation

1.  **Clone the repository (if applicable):**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  **Install the required packages:**

    ```bash
    pip install streamlit PyPDF2 pandas langchain langchain-google-genai faiss-cpu
    ```

3.  **Obtain a Google Gemini API key:**

    -      Go to [Google AI Studio](https://ai.google.dev/).
    -      Create a project and obtain an API key.

## How to Run

1.  **Save the Python script:** Save the Python code you provided as a `.py` file (e.g., `pdf_chat.py`).

2.  **Open your terminal or command prompt:** Navigate to the directory where you saved the Python script.

3.  **Run the Streamlit application:** Execute the following command:

    ```bash
    streamlit run pdf_chat.py
    ```

    Streamlit will launch a local server and open the application in your default web browser.

4.  **Use the application:** Follow the on-screen instructions to upload PDF files, enter your API key, and ask questions.

## Usage

1.  **Enter your Google Gemini API key:**

    -      In the sidebar, enter your Google Gemini API key in the provided text input.

2.  **Upload PDF files:**

    -      Click the "Browse files" button to upload one or more PDF files.
    -   Click the "Submit & Process" button.

3.  **Ask questions:**

    -      In the text input field, type your question and press Enter.

4.  **View answers and conversation history:**

    -      The application will display the answer and add the question and answer to the conversation history.

5.  **Download conversation history:**

    -      Click the "Download conversation history as CSV file" button in the sidebar to download the conversation history.

6.  **Reset or Rerun:**

    -   Use the reset and rerun buttons in the sidebar for those functions.

## Code Explanation

-   `get_pdf_text(pdf_docs)`: Extracts text from uploaded PDF files.
-   `get_text_chunks(text, model_name)`: Splits the extracted text into smaller chunks.
-   `get_vector_store(text_chunks, model_name, api_key=None)`: Creates a vector store (FAISS) from the text chunks.
-   `get_conversational_chain(model_name, vectorstore=None, api_key=None)`: Creates a question-answering chain using LangChain and Google's generative AI models.
-   `user_input(user_question, model_name, api_key, pdf_docs, conversation_history)`: Processes the user's question, retrieves relevant information, and generates a response.
-   `main()`: Sets up the Streamlit application and handles user interactions.

## Dependencies

-   Streamlit
-   PyPDF2
-   Pandas
-   LangChain
-   Langchain Google Genai
-   FAISS

## Notes

-   Ensure you have a valid Google Gemini API key.
-   The application uses FAISS for vector storage, which is stored locally in the `faiss_index` directory.
-   The application handles multiple uploaded PDF files.
-   Error handling is included to ensure a smooth user experience.
-   The application uses custom CSS to style the chat interface.
-   The application provides download functionality for the chat history.


