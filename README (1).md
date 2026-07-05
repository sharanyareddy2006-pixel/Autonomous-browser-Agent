# Autonomous Browser Agent – LLM-Powered Web Automation

An AI-powered browser automation agent that understands natural-language instructions and autonomously navigates websites, interacts with page elements, and extracts content — without any manual scripting.

## What it does

Give it a plain-English task like:

> "Go to google.com, search for 'geeksforgeeks', click search, and return the first result URL."

...and the agent independently plans the steps, navigates the browser, interacts with the correct elements, and returns the result — powered by an LLM reasoning loop that decides the next action at each step.

## Key features

- **Natural-language task execution** — no selectors, no scripts, just describe the task
- **Multi-LLM support** — configured and tested across OpenAI, Google Gemini, and Groq, with automatic fallback handling for provider-specific quirks
- **Zero-cost inference** — engineered an OpenAI-compatible routing setup to run Groq's LLaMA 3.3 70B model, avoiding paid API costs entirely
- **Stable Windows deployment** — resolved environment, dependency, and memory-module conflicts for a reliable end-to-end pipeline
- **Web UI** — simple browser-based interface to configure the LLM provider/model and submit tasks

## Tech stack

Python · browser-use · LangChain · Gradio · Playwright · Groq API (LLaMA 3.3 70B)

## Running it locally

```bash
git clone <this-repo-url>
cd web-ui
uv venv --python 3.11
.venv\Scripts\activate      # Windows
uv pip install -r requirements.txt
playwright install --with-deps
copy .env.example .env      # add your API keys
python webui.py --ip 127.0.0.1 --port 7788
```

Then open `http://127.0.0.1:7788` in your browser.

## Demo

*(Add a screenshot or the agent_history GIF here once uploaded)*

---

Built on the [browser-use](https://github.com/browser-use/web-ui) framework.
