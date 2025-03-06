# AI Agent

## Installation Guide

### Prerequisites
- Python 3.11 or higher
- Git (for cloning the repository)

## Clone the Repository
Since this repository contains a submodule (`web-ui`), you need to clone it with submodules:
```bash
git clone --recurse-submodules https://github.com/mouli4401/ai_agent.git
cd ai_agent
```

If you have already cloned the repository without submodules, initialize the submodule manually:
```bash
git submodule update --init --recursive
```

## Set Up Python Environment
We recommend using `uv` for managing the Python environment.

Using `uv` (recommended):
```bash
uv venv --python 3.11
```

Activate the virtual environment:
- **Windows (Command Prompt):**
  ```bash
  .venv\Scripts\activate
  ```
- **Windows (PowerShell):**
  ```bash
  .\.venv\Scripts\Activate.ps1
  ```
- **macOS/Linux:**
  ```bash
  source .venv/bin/activate
  ```

## Install Dependencies
```bash
uv pip install -r requirements.txt
```

## Install Playwright (If Required)
```bash
playwright install
```

## Configure Environment
Create a copy of the example environment file:
```bash
cp .env.example .env
```

Edit `.env` and add API keys and necessary settings.

## Running the Application
### Local Setup
```bash
python webui.py --ip 127.0.0.1 --port 7788
```
- Access the Web UI at: [http://127.0.0.1:7788](http://127.0.0.1:7788)

### Using Docker (Optional)
**Prerequisites:** Docker & Docker Compose must be installed.

```bash
docker compose up --build
```

To keep the browser session persistent:
```bash
CHROME_PERSISTENT_SESSION=true docker compose up --build
```

## Updating the Submodule
If `web-ui` receives updates, pull the latest changes using:
```bash
git submodule update --remote --merge
```

## Removing the Submodule (If Needed)
If you need to remove `web-ui`:
```bash
git rm --cached web-ui
rm -rf web-ui
```

---

This guide ensures proper handling of the `web-ui` submodule within your `ai_agent` repository. 🚀

