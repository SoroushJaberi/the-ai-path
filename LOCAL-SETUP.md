# Local Setup (optional)

Colab is all you need for this course. This guide is for the **Episode 01 Stretch mission**, or for anyone who wants to run notebooks on their own computer.

**Checked:** 21 Oct 2026. Tools change, so if a step fails, check the date and open an issue.

---

## Why we pin Python 3.13

Colab runs **Python 3.13** (Colab release notes, 16 Sep 2026). We use the same version locally, so your results match the videos.
Newer Python releases sometimes arrive before every library supports them. Pinning the version removes that whole class of problems. That's the lesson of Episode 01.

This repo includes a `.python-version` file containing `3.13`, and the tools below read it automatically.

## 1. Install uv (a fast Python and package manager)

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

**macOS / Linux:**
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Close and reopen your terminal, then check:
```bash
uv --version
```

Official guide: [docs.astral.sh/uv](https://docs.astral.sh/uv/getting-started/installation/)

## 2. Get this repo

Install [Git](https://git-scm.com/downloads), then clone **your fork** (replace `YOUR-USERNAME`):
```bash
git clone https://github.com/YOUR-USERNAME/the-ai-path.git
cd the-ai-path
```

## 3. Create the environment for an episode

From inside the `the-ai-path` folder:
```bash
uv venv
uv pip install -r season-01/ep-01-first-model/requirements.txt
```

`uv venv` creates a `.venv` folder using Python 3.13 (from `.python-version`), downloading it if needed.
Every episode folder has its own `requirements.txt` with **exact pinned versions**.

## 4. Open notebooks in VS Code

1. Install [VS Code](https://code.visualstudio.com/) and its **Python** and **Jupyter** extensions.
2. Open the `the-ai-path` folder in VS Code.
3. Open an episode's `lesson.ipynb`, click **Select Kernel** (top-right), and choose the `.venv` environment.
4. Run all cells from the top. They should behave exactly as they do in Colab.

## Troubleshooting

- **`uv` not found:** close and reopen the terminal after installing.
- **Windows blocks `.venv\Scripts\activate`:** you don't need to activate. VS Code can use `.venv` directly (step 4).
- **Wrong Python version:** run `uv python list` to see what's installed, and make sure `.python-version` says `3.13`.
- **A package fails to install:** check that you're installing from the episode's `requirements.txt`, not the latest versions.
