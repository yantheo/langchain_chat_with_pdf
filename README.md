# 💬 LangChain Chat-with-Multi-PDF App

## Introduction

This is an interactive application built using **Streamlit** and **LangChain** that allows users to upload and chat with the content of **multiple PDF documents** simultaneously. The application leverages the power of OpenAI's GPT model to generate contextual answers based solely on the information extracted from the provided documents.

## 🚀 Key Features

* **Multi-Document Chat:** Ask questions spanning all uploaded PDF documents.
* **Simple User Interface:** Powered by Streamlit, the interface is easy to use for document uploading and conversation.
* **Vectorization & Indexing:** Utilizes the LangChain architecture to create a vector index of the documents, ensuring fast and relevant information retrieval (RAG - Retrieval-Augmented Generation).

## 🛠️ Prerequisites

To run this application, you must have Python installed (version 3.8+ recommended) and an OpenAI account for the API key.

### 1. API Key Requirement

This application requires an OpenAI API key to access the language models and embedding models.

* **Key Name:** The application looks for the environment variable named `OPENAI_API_KEY`.

## ⚙️ Setup and Running the Application

Follow these steps to set up and run the application on your local machine.

### Step 1: Clone the Repository

Clone this Git repository to your local machine:

```bash
git clone [YOUR REPOSITORY URL]
cd LANGCHAIN
Step 2: Create the Virtual Environment
It is highly recommended to use a virtual environment to isolate project dependencies.

Bash

python3 -m venv venv
Step 3: Activate the Environment
macOS/Linux

Bash

source venv/bin/activate
Windows (PowerShell)

Bash

.\venv\Scripts\Activate.ps1
Step 4: Install Dependencies
Install all required packages listed in the requirements.txt file:

Bash

pip install -r requirements.txt
Step 5: Configure the API Key
Create a file named .env at the root of the project (LANGCHAIN/) and add your OpenAI API key, as follows:

# .env file
OPENAI_API_KEY="your_secret_api_key_here"
(Note: The file .env is ignored by Git via .gitignore to protect your sensitive key.)

Step 6: Launch the Streamlit Application
Ensure your virtual environment is active (see Step 3), then launch the application by pointing to the main script inside the src/ folder:

Bash

streamlit run src/app.py
The application should automatically open in your default browser (usually at http://localhost:8501).

📁 Project Structure
This structure reflects the best practices used to organize the application:

LANGCHAIN/
├── .gitignore          # Files to ignore (venv/, .env, etc.)
├── README.md           # This file
├── requirements.txt    # List of Python dependencies
├── venv/               # Virtual environment (ignored by Git)
├── .env                # Environment variables / API Key (ignored by Git)
└── src/                # Folder containing the application source code
    ├── app.py          # Main Streamlit entry point
    ├── htmlTemplate.py # HTML/CSS code for the chat interface
    └── __init__.py     # Python package marker
