# Agentic AI Teaching Assistant

An AI-powered teaching assistant built with **Python, Django, Ollama, and Llama 3.2**. It helps students learn Python programming and AI-related subjects through interactive conversations and step-by-step explanations.

## Overview

The Agentic AI Teaching Assistant is a web-based application that connects a Django backend to a locally hosted Large Language Model (LLM) through Ollama.

Users can ask questions, receive explanations, explore programming concepts, and revisit previous conversations.

## Features

- **AI-powered chat:** Interactive conversations using the Llama 3.2 model.
- **Python tutoring:** Learn Python concepts with practical examples and step-by-step code explanations.
- **AI learning support:** Assistance with Artificial Intelligence, Machine Learning, Deep Learning, IoT, and Agentic AI concepts.
- **Conversation history:** Save and revisit previous chat sessions.
- **Session-based context:** Use previous messages in the selected conversation to maintain context.
- **Request validation:** Validate chat requests using Pydantic.
- **Dashboard:** Access the application's learning and chat interface.

## Application Screenshots

### Dashboard

![Application Dashboard](screenshots/dashboard.png)

### AI Chat Interface

![AI Chat Interface](screenshots/chat.png)

### Conversation History

![Conversation History](screenshots/history.png)

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Django | Backend web framework |
| Ollama | Local LLM integration |
| Llama 3.2 (3B) | Language model |
| Pydantic | Request validation |
| SQLite | Database |
| HTML, CSS, JavaScript | Frontend |

## System Architecture

```text
          User
            |
            v
     Web Interface
            |
            v
      Django Backend
            |
       +----+----+
       |         |
       v         v
   Pydantic   SQLite
   Validation  Database
       |
       v
    AI Engine
       |
       v
     Ollama
       |
       v
   Llama 3.2
       |
       v
  AI-generated Response
       |
       v
   Web Interface
```

## Project Structure

```text
Agentic_AI_Project/
│
├── screenshots/
│   ├── dashboard.png
│   ├── chat.png
│   └── history.png
│
├── config/
│   ├── manage.py
│   ├── requirements.txt
│   │
│   ├── assistant/
│   │   ├── migrations/
│   │   ├── ai_engine.py
│   │   ├── models.py
│   │   ├── schemas.py
│   │   ├── views.py
│   │   └── urls.py
│   │
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── asgi.py
│   │   └── wsgi.py
│   │
│   ├── templates/
│   └── static/
│
├── .gitignore
└── README.md
```

## Installation and Setup

### Prerequisites

- Python 3.12 or a compatible Python version
- Git
- Ollama

### 1. Clone the repository

```bash
[git clone https://github.com/pruthvirajsingh01/Agentic_AI_Project
cd Agentic_AI_Project
```

### 2. Navigate to the Django project

```bash
cd config
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows PowerShell:

```powershell
.\venv\Scripts\Activate
```

### 4. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 5. Configure the Django secret key

In PowerShell, generate and save a secret key:

```powershell
$SECRET = python -c "import secrets; print(secrets.token_urlsafe(50))"
setx SECRET_KEY "$SECRET"
$env:SECRET_KEY = $SECRET
```

Keep the secret key private. Do not commit it to GitHub.

### 6. Install and configure Ollama

Download and install Ollama:

https://ollama.com/

Download the model:

```bash
ollama pull llama3.2:3b
```

Make sure the Ollama service is running.

### 7. Apply database migrations

```bash
python manage.py migrate
```

### 8. Start the Django development server

```bash
python manage.py runserver
```

### 9. Open the application

Visit:

http://127.0.0.1:8000/

## Future Improvements

- Persistent long-term conversational memory
- Multi-agent workflow integration
- Support for additional language models
- Improved context management
- User authentication
- Automated testing
- Cloud deployment

## Author

## Project Maintainer

Pruthviraj Singh

GitHub: https://github.com/pruthvirajsingh01
linkedin.com/in/pruthviraj-singh-050414421  

## License

This project is available for educational and learning purposes.
