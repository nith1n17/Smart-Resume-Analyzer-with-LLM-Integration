📃 AI Resume Critiquer

#-ai-resume-critiquer

An AI-powered resume feedback tool built with Streamlit and integrated with modern LLM APIs. Upload a resume, optionally specify a target job role, and receive structured, actionable feedback in seconds.

📖 Overview

#-overview

AI Resume Critiquer is a lightweight Streamlit application designed to demonstrate practical LLM integration in a real-world use case: resume evaluation. Instead of relying on generic checklists, the app sends the actual resume content to a large language model and returns tailored, structured feedback on content clarity, skills presentation, and experience descriptions.

The application accepts a PDF or TXT resume and automatically:

Extracts and parses the raw text from the uploaded file
Builds a structured prompt combining resume content and (optionally) a target job role
Sends the prompt to an LLM via the OpenRouter API
Returns clear, actionable feedback directly in the Streamlit interface

This project was built as a hands-on demonstration of prompt engineering, API integration, and building a usable LLM-powered application from scratch.

🚀 Features

#-features

Multi-format resume upload — accepts both PDF and TXT files
PDF text extraction — parses resume content using PyPDF2
Role-targeted feedback — optionally specify a job role for context-aware analysis
LLM-powered critique — structured feedback covering:
Content clarity and impact
Skills presentation
Experience descriptions
Role-specific improvement suggestions
Secure API key handling — credentials managed via environment variables, never hardcoded
Graceful error handling — handles empty files, API errors, and empty model responses without crashing
🏗 Project Architecture

#-project-architecture

        Resume Upload (PDF / TXT)
                  │
                  ▼
        Text Extraction Layer
           (PyPDF2 / raw text)
                  │
                  ▼
         Prompt Construction
    (resume content + target role)
                  │
                  ▼
      LLM API Call (via OpenRouter)
                  │
                  ▼
      Structured Feedback Response
                  │
                  ▼
       Streamlit Results Display
📂 Project Structure

#-project-structure

Smart-Resume-Analyzer-with-LLM-Integration/

│
├── main.py            # Core Streamlit application
├── pyproject.toml     # Project dependencies and metadata
├── uv.lock            # Locked dependency versions
├── .env.example        # Template for required environment variables
├── README.md
└── .gitignore
⚙ Technologies Used

#-technologies-used

Technology	Purpose
Python	Core application logic
Streamlit	Web interface
OpenAI SDK	LLM client (routed via OpenRouter)
OpenRouter API	Access to free/paid LLM models
PyPDF2	PDF text extraction
python-dotenv	Environment variable management
🔄 Workflow

#-workflow

User uploads resume (PDF/TXT)
          │
          ▼
Extract raw text content
          │
          ▼
Enter target job role (optional)
          │
          ▼
Construct analysis prompt
          │
          ▼
Send prompt to LLM via OpenRouter
          │
          ▼
Display structured feedback in UI
💻 Installation

#-installation

Clone the repository

bash
git clone https://github.com/nith1n17/Smart-Resume-Analyzer-with-LLM-Integration.git

Navigate into the project

bash
cd Smart-Resume-Analyzer-with-LLM-Integration

Create a virtual environment

bash
python -m venv .venv

Activate the environment

macOS/Linux

bash
source .venv/bin/activate

Windows

bash
.venv\Scripts\activate

Install dependencies

bash
pip install -r requirements.txt

If using uv instead of pip, run uv sync to install dependencies from pyproject.toml and uv.lock.

Create a .env file in the project root

OPENROUTER_API_KEY=YOUR_OPENROUTER_API_KEY

Run the application

bash
streamlit run main.py
🔑 Getting an API Key

#-getting-an-api-key

This project uses OpenRouter to access LLM models (including free-tier models):

Create a free account at openrouter.ai
Generate an API key from your account dashboard
Add it to your .env file as OPENROUTER_API_KEY
📚 Key Concepts Demonstrated

#-key-concepts-demonstrated

LLM API integration
Prompt engineering for structured, consistent outputs
PDF/text parsing and preprocessing
Environment variable management for secure credential handling
Streamlit UI development
Defensive error handling for file uploads and API responses
🚀 Future Improvements

#-future-improvements

Planned enhancements include:

Support for DOCX resume uploads
ATS compatibility scoring
Resume-to-job-description matching
Downloadable feedback reports (PDF export)
Support for multiple LLM providers/models via a dropdown
Highlighted inline suggestions instead of plain-text feedback
👨‍💻 Author

#‍-author

Nithin

A portfolio project demonstrating practical skills in LLM integration, prompt engineering, and application development.

GitHub: github.com/nith1n17
LinkedIn: linkedin.com/in/nithinsv17
⭐ If you found this project useful, consider giving it a star!

#-if-you-found-this-project-useful-consider-giving-it-a-star
