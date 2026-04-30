<p align="center">
  <img src="./assets/web-ui.png" alt="Operator From BrowserUse UI" width="100%" />
</p>

<h1 align="center">Operator From BrowserUse</h1>
<p align="center"><strong>Orchestrate AI browser agents with a polished, production-ready Web UI.</strong></p>
<p align="center">Run tasks with your preferred LLM, bring your own browser profile, and watch live runs in real time.</p>

<p align="center">
  <a href="https://img.shields.io/badge/build-passing-brightgreen"><img src="https://img.shields.io/badge/build-passing-brightgreen" alt="Build" /></a>
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT" /></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/python-3.11%2B-blue" alt="Python 3.11+" /></a>
  <a href="https://www.gradio.app/"><img src="https://img.shields.io/badge/Gradio-5.x-orange" alt="Gradio" /></a>
  <a href="https://www.docker.com/"><img src="https://img.shields.io/badge/docker-ready-2496ED" alt="Docker" /></a>
</p>

---

## 🚀 Project Overview

Operator From BrowserUse is a modern Web UI for running **browser-use** agents without writing scripts. It turns complex browser automation into a clean, visual workflow so teams can prototype, test, and operate AI-driven tasks confidently.

**In 60 seconds, you should know:**
- **What it does:** Launches AI browser agents through a Gradio interface with live visibility.
- **Why it matters:** Reduces setup friction and makes agent runs observable, repeatable, and shareable.
- **Key features:** Multi-LLM support, persistent browser sessions, recordings, and VNC view.
- **Tech stack:** Python 3.11+, Gradio, Playwright, browser-use, Docker.

## ✨ Features

- **Multi-LLM support**: OpenAI, Azure OpenAI, Anthropic, Google, DeepSeek, Mistral, Ollama, and more.
- **Bring your own browser**: Reuse existing profiles to avoid repeated logins.
- **Persistent sessions**: Keep the browser open between runs for continuity.
- **Live observability**: Watch runs in real time through a VNC viewer.
- **Recording & traces**: Capture videos, histories, and traces for audits or demos.
- **Clean UI controls**: Tuning knobs for models, steps, vision, and tool-calling.

## 🧠 Problem & Solution

**Problem:** Running browser automation agents typically requires scripts, local configs, and limited visibility into what the agent is doing. This slows iteration and reduces trust.

**Solution:** Operator From BrowserUse provides a professional Web UI that centralizes configuration, execution, and monitoring—so anyone can launch, watch, and refine browser-based AI tasks in minutes.

## 🛠 Tech Stack

- **Frontend/UI:** Gradio 5.x
- **Agent Engine:** browser-use
- **Browser Automation:** Playwright
- **LLM Integrations:** OpenAI, Azure OpenAI, Anthropic, Google, DeepSeek, Mistral, Ollama
- **Runtime:** Python 3.11+
- **Deployment:** Docker & Docker Compose

## 📸 Screenshots / Demo

<p align="center">
  <img src="./assets/web-ui.png" alt="Operator From BrowserUse UI" width="100%" />
</p>

## ⚙️ Installation & Setup

### Prerequisites
- Python **3.11+**
- Git
- (Optional) Docker + Docker Compose

### Option 1: Local Installation

```bash
# Clone the repository
git clone https://github.com/your-org/Operator-From-BrowserUse.git
# Replace with the canonical repository URL for your organization.
cd Operator-From-BrowserUse

# Create a virtual environment (recommended)
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install Playwright browsers
playwright install
```

Create your environment file:
```bash
cp .env.example .env
```

Run the Web UI:
```bash
python webui.py --ip 127.0.0.1 --port 7788
```

Open **http://127.0.0.1:7788** in your browser. Common flags: `--theme` (UI styling), `--dark-mode` (dark UI), `--ip`/`--port` (bind address). For the full list, run `python webui.py --help`.

### Option 2: Docker Installation

```bash
# Clone the repository
git clone https://github.com/your-org/Operator-From-BrowserUse.git
# Replace with the canonical repository URL for your organization.
cd Operator-From-BrowserUse

# Create environment file
cp .env.example .env

# Build and start
docker compose up --build
```

Access:
- **Web UI:** http://localhost:7788
- **VNC Viewer:** http://localhost:6080/vnc.html (password in `.env`)

## 📂 Project Structure

```
.
├── assets/                # Images and demos
├── src/                   # Core application logic
│   ├── agent/             # Custom agents and prompts
│   ├── browser/           # Browser and context extensions
│   ├── controller/        # UI and orchestration controller
│   └── utils/             # Helpers, configs, and LLM utilities
├── tests/                 # Test suite (requires API keys from .env.example)
├── webui.py               # Gradio entrypoint
├── docker-compose.yml     # Container setup
└── requirements.txt       # Python dependencies
```

## 🔮 Future Improvements

- Role-based access & authentication
- Task templates and reusable workflows
- Session sharing & run history dashboard
- Cloud deployment guide and one-click hosting

## 🤝 Contribution Guidelines

Contributions are welcome!

1. Fork the repo and create your feature branch.
2. Keep changes focused and well-tested.
3. Run the test suite to verify your change: `pytest` (requires API keys from `.env.example` and Playwright browsers installed).
4. Open a PR with a clear description of the change.

## 📜 License

Distributed under the **MIT License**. See [LICENSE](./LICENSE) for details.

---

Built on top of the amazing [browser-use](https://github.com/browser-use/browser-use) ecosystem.
