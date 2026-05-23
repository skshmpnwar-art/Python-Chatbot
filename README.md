<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=200&section=header&text=🤖%20Python%20GPT%20Chatbot&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=An%20AI-powered%20conversational%20assistant%20built%20with%20Python%20%26%20OpenAI&descAlignY=58&descSize=16" alt="Header Banner" width="100%"/>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenAI-GPT--4-412991?style=for-the-badge&logo=openai&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Active-22c55e?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/PRs-Welcome-f97316?style=for-the-badge"/>
</p>

<p align="center">
  <a href="#-overview">Overview</a> •
  <a href="#-features">Features</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-prerequisites">Prerequisites</a> •
  <a href="#-installation">Installation</a> •
  <a href="#-usage">Usage</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-contributing">Contributing</a>
</p>

</div>

---

## 🧠 Overview

**Python GPT Chatbot** is a fully-featured, conversational AI assistant powered by OpenAI's GPT models. Built entirely in Python, it supports multi-turn conversations, persistent memory, customizable system prompts, and can be deployed as a CLI tool, REST API, or integrated into a web interface.

Whether you're building a customer support bot, a personal assistant, or experimenting with LLMs — this project provides a clean, extensible foundation.

<div align="center">
  <img src="https://images.unsplash.com/photo-1677442135703-1787eea5ce01?w=900&h=400&fit=crop&q=80" alt="AI Chatbot Concept" width="85%" style="border-radius: 12px; margin: 16px 0;"/>
  <br/>
  <em>Conversational AI at your fingertips</em>
</div>

---

## ✨ Features

| Feature | Description |
|---|---|
| 🗣️ **Multi-turn Conversations** | Maintains full conversation context across multiple exchanges |
| 💾 **Conversation History** | Save and load past chats from JSON files |
| 🎭 **Custom System Prompts** | Define the chatbot's persona and behaviour |
| 🌐 **REST API Mode** | Expose the chatbot via FastAPI endpoints |
| 🖥️ **CLI Interface** | Run it directly in your terminal |
| 🔑 **Secure API Key Handling** | Uses `.env` files — no hardcoded secrets |
| 🔁 **Streaming Responses** | Real-time token streaming like ChatGPT |
| 📊 **Token Usage Tracking** | Monitor prompt/completion token consumption |
| 🧩 **Model Switching** | Easily swap between GPT-3.5, GPT-4, GPT-4o |
| 🐳 **Docker Support** | One-command containerised deployment |

---

## 🛠️ Tech Stack

<div align="center">

### Core Technologies

<img src="https://skillicons.dev/icons?i=python,fastapi,docker,git,github,vscode&theme=dark" alt="Tech Stack Icons"/>

</div>

| Technology | Purpose | Version |
|---|---|---|
| ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) | Core language | `3.9+` |
| ![OpenAI](https://img.shields.io/badge/OpenAI%20SDK-412991?logo=openai&logoColor=white) | GPT model access | `>=1.0.0` |
| ![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white) | REST API framework | `>=0.100.0` |
| ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?logo=pydantic&logoColor=white) | Data validation | `>=2.0` |
| ![dotenv](https://img.shields.io/badge/python--dotenv-ECD53F?logo=dotenv&logoColor=black) | Environment variables | `>=1.0.0` |
| ![Uvicorn](https://img.shields.io/badge/Uvicorn-499848?logo=gunicorn&logoColor=white) | ASGI server | `>=0.22.0` |
| ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) | Containerisation | `>=20.0` |
| ![Rich](https://img.shields.io/badge/Rich-CLI-6366f1?logoColor=white) | Beautiful terminal UI | `>=13.0.0` |

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed and configured:

<div align="center">
  <img src="https://images.unsplash.com/photo-1607799279861-4dd421887fb3?w=900&h=350&fit=crop&q=80" alt="Development Setup" width="85%" style="border-radius: 12px; margin: 16px 0;"/>
  <br/>
  <em>A modern development environment ready for AI integration</em>
</div>

### ✅ System Requirements

- **OS**: Windows 10/11, macOS 11+, or Ubuntu 20.04+
- **RAM**: Minimum 4 GB (8 GB recommended)
- **Disk**: ~500 MB free space
- **Internet**: Required for OpenAI API calls

### ✅ Software Requirements
✔  Python        3.9 or higher
✔  pip           Latest version
✔  Git           2.x or higher
✔  Docker        20.x+ (optional, for containerised deployment)
✔  VS Code       Recommended editor
### ✅ API & Accounts

| Requirement | Where to Get It |
|---|---|
| 🔑 **OpenAI API Key** | [platform.openai.com](https://platform.openai.com/api-keys) |
| 💳 **OpenAI Billing** | Add a payment method to your OpenAI account |
| 🐙 **GitHub Account** | [github.com](https://github.com) (to fork/clone) |

> **💡 Tip:** New OpenAI accounts often come with free credits — enough to get started immediately!

---

## 🚀 Installation

### Step 1 — Clone the Repository

```bash
git clone https://github.com/yourusername/python-gpt-chatbot.git
cd python-gpt-chatbot
```

### Step 2 — Create a Virtual Environment

```bash
# Create virtual environment
python -m venv venv

# Activate it
# On macOS/Linux:
source venv/bin/activate

# On Windows:
venv\Scripts\activate
```

### Step 3 — Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4 — Set Up Environment Variables

```bash
# Copy the example env file
cp .env.example .env
```

Then open `.env` and fill in your details:

```env
OPENAI_API_KEY=sk-your-api-key-here
MODEL_NAME=gpt-4o
MAX_TOKENS=1000
TEMPERATURE=0.7
SYSTEM_PROMPT=You are a helpful and friendly assistant.
```

---

## 📁 Project Structure
python-gpt-chatbot/
│
├── 📂 src/
│   ├── 🐍 chatbot.py          # Core chatbot logic & OpenAI integration
│   ├── 🐍 api.py              # FastAPI REST endpoints
│   ├── 🐍 memory.py           # Conversation history management
│   ├── 🐍 config.py           # Configuration & environment loader
│   └── 🐍 utils.py            # Helper utilities & token counter
│
├── 📂 tests/
│   ├── 🧪 test_chatbot.py     # Unit tests for core logic
│   └── 🧪 test_api.py         # API endpoint tests
│
├── 📂 data/
│   └── 📂 conversations/      # Saved conversation histories (JSON)
│
├── 📂 docs/
│   └── 📄 api_reference.md    # API documentation
│
├── 🐍 main.py                 # Entry point — CLI chatbot
├── 🐋 Dockerfile              # Docker image definition
├── 🐋 docker-compose.yml      # Multi-service Docker setup
├── 📄 requirements.txt        # Python dependencies
├── 📄 .env.example            # Environment variable template
├── 📄 .gitignore              # Git ignore rules
└── 📄 README.md               # This file!

---

## 💻 Usage

### 🖥️ CLI Mode

Run the chatbot directly in your terminal:

```bash
python main.py
```

<div align="center">
  <img src="https://images.unsplash.com/photo-1629654291663-b91ad427698f?w=900&h=350&fit=crop&q=80" alt="Terminal CLI" width="85%" style="border-radius: 12px; margin: 16px 0;"/>
  <br/>
  <em>Interactive CLI powered by the Rich library</em>
</div>

**Example session:**

🤖 Python GPT Chatbot — Type 'quit' to exit, 'history' to view chat log
You: Hello! Who are you?
Assistant: Hi there! I'm your AI-powered assistant built with Python and GPT-4.
How can I help you today?
You: Explain recursion in Python.
Assistant: Great question! Recursion is when a function calls itself...
You: quit
Goodbye! 👋

### 🌐 API Mode

Start the FastAPI server:

```bash
uvicorn src.api:app --reload --port 8000
```

Then open your browser at `http://localhost:8000/docs` for the interactive Swagger UI.

**Send a message via API:**
```bash
curl -X POST "http://localhost:8000/chat" \
     -H "Content-Type: application/json" \
     -d '{"message": "What is machine learning?", "session_id": "user_001"}'
```

**Response:**
```json
{
  "session_id": "user_001",
  "response": "Machine learning is a branch of AI...",
  "tokens_used": 142,
  "model": "gpt-4o"
}
```

### 🐳 Docker Mode

```bash
# Build and run with Docker Compose
docker-compose up --build
```

---

## 🔧 Configuration Options

| Variable | Default | Description |
|---|---|---|
| `OPENAI_API_KEY` | *(required)* | Your OpenAI secret key |
| `MODEL_NAME` | `gpt-4o` | GPT model to use |
| `MAX_TOKENS` | `1000` | Max tokens per response |
| `TEMPERATURE` | `0.7` | Creativity (0.0 = deterministic, 1.0 = creative) |
| `SYSTEM_PROMPT` | *"You are a helpful assistant."* | Sets the chatbot's persona |
| `MAX_HISTORY` | `20` | Max conversation turns to keep in memory |
| `STREAM` | `true` | Enable/disable streaming responses |

---

## 🧪 Running Tests

```bash
# Run all tests
pytest tests/ -v

# Run with coverage report
pytest tests/ --cov=src --cov-report=html
```

---

## 📦 Dependencies

All dependencies are listed in `requirements.txt`:
openai>=1.0.0
fastapi>=0.100.0
uvicorn>=0.22.0
pydantic>=2.0
python-dotenv>=1.0.0
rich>=13.0.0
pytest>=7.0.0
pytest-cov>=4.0.0
httpx>=0.24.0

Install them all at once:

```bash
pip install -r requirements.txt
```

---

## 🗺️ Roadmap

- [x] Core GPT chat integration
- [x] Multi-turn conversation memory
- [x] CLI interface with Rich
- [x] FastAPI REST endpoints
- [x] Streaming responses
- [x] Docker support
- [ ] Web UI (Streamlit / Gradio)
- [ ] Plugin / tool-calling support
- [ ] Voice input/output (Whisper + TTS)
- [ ] RAG (Retrieval-Augmented Generation) support
- [ ] Fine-tuning pipeline

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. **Fork** the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a **Pull Request**

Please make sure to:
- Follow the existing code style
- Add/update tests as needed
- Update documentation where relevant

---

## 🔒 Security

- **Never** commit your `.env` file or API keys to version control
- `.gitignore` already excludes `.env` by default
- Rotate your OpenAI API key if it is ever exposed
- Consider rate-limiting your API endpoints in production

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 💬 Support & Contact

<div align="center">

If you found this project helpful, please consider ⭐ **starring the repository** — it means a lot!

[![GitHub Stars](https://img.shields.io/github/stars/yourusername/python-gpt-chatbot?style=social)](https://github.com/yourusername/python-gpt-chatbot)
[![GitHub Forks](https://img.shields.io/github/forks/yourusername/python-gpt-chatbot?style=social)](https://github.com/yourusername/python-gpt-chatbot)

Have a question? Open an [Issue](https://github.com/yourusername/python-gpt-chatbot/issues) or start a [Discussion](https://github.com/yourusername/python-gpt-chatbot/discussions).

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=100&section=footer" width="100%"/>

</div>
