# SETUP.md — ProfessorGPT Installation & Deployment Guide

## Prerequisites

- Python 3.11 or higher
- pip (comes with Python)
- An [Anthropic API key](https://console.anthropic.com/) (required)
- An [OpenAI API key](https://platform.openai.com/) (optional — only for audio transcription)

---

## Local Development Setup

### Step 1 — Clone the repository
```bash
git clone https://github.com/your-group/professorgpt.git
cd professorgpt
```

### Step 2 — Create a virtual environment (recommended)
```bash
python -m venv venv

# Activate (macOS/Linux)
source venv/bin/activate

# Activate (Windows)
venv\Scripts\activate
```

### Step 3 — Install dependencies
```bash
pip install -r requirements.txt
```

### Step 4 — Configure your API key

Create a `.env` file in the project root:
```bash
cp .env.example .env
```

Edit `.env` and add your keys:
```
ANTHROPIC_API_KEY=sk-ant-...your-key-here...
OPENAI_API_KEY=sk-...your-key-here...  # optional
```

> ⚠️ Never commit `.env` to GitHub. It is listed in `.gitignore`.

### Step 5 — Run the application
```bash
streamlit run src/app.py
```

The app opens automatically at **http://localhost:8501**

---

## Deployment Options

### Option A — Streamlit Community Cloud (Recommended, Free)

1. Push your repo to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io)
3. Click **New app** → select your repo → set `src/app.py` as the main file
4. Under **Advanced settings → Secrets**, add:
   ```toml
   ANTHROPIC_API_KEY = "sk-ant-..."
   ```
5. Click **Deploy** — your app will be live at `https://your-app.streamlit.app`

### Option B — Railway

1. Install the Railway CLI: `npm install -g @railway/cli`
2. `railway login`
3. `railway init` (in project root)
4. Set environment variable in Railway dashboard: `ANTHROPIC_API_KEY`
5. `railway up`

### Option C — Docker

```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY src/ ./src/
EXPOSE 8501
CMD ["streamlit", "run", "src/app.py", "--server.port=8501", "--server.address=0.0.0.0"]
```

```bash
docker build -t professorgpt .
docker run -p 8501:8501 -e ANTHROPIC_API_KEY=your_key professorgpt
```

---

## Environment Variables Reference

| Variable | Required | Description |
|----------|----------|-------------|
| `ANTHROPIC_API_KEY` | ✅ Yes | Claude API key from console.anthropic.com |
| `OPENAI_API_KEY` | ❌ Optional | For Whisper audio transcription |

---

## Troubleshooting

**`ModuleNotFoundError: anthropic`**  
→ Make sure your virtual environment is activated: `source venv/bin/activate`  
→ Then: `pip install -r requirements.txt`

**`AuthenticationError: Invalid API key`**  
→ Check your `.env` file has no extra spaces around the `=`  
→ Restart Streamlit after changing `.env`

**App loads but AI features return errors**  
→ Verify your Anthropic API key has credits at [console.anthropic.com](https://console.anthropic.com)

**Audio files not transcribing**  
→ Whisper integration requires `OPENAI_API_KEY` — see Step 4 above
