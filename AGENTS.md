# AGENTS.md

Instructions for AI coding agents (Claude Code, Codex, and others) working in this repository. `CLAUDE.md` imports this file. Fill in the sections marked TODO when the project is set up, and keep them current.

## Project overview

TODO: what the project studies, the main research questions, and the data sources.

## Environment

- Python dependencies are managed with uv. Run `uv sync` after pulling changes.
- Run Python through the project environment: `uv run python ...`, `uv run jupyter lab`, `uv run snakemake -j 1`.
- Add dependencies with `uv add <package>`. Never use `pip install` directly.
- Reusable code goes in the package under `libs/`, which is installed in editable mode.

## Running the pipeline

TODO: the main commands, the order of steps, and the final outputs.

## Data

TODO: where each dataset lives (in `data/` or on a remote server), and which files are read-only.

- Never modify files in `data/raw/`.
- Never commit large or sensitive data files, or anything under `data/interim/`, `data/processed/`, or `data/external/`.
- Document new datasets in `data/README.md`.

## Rules

- Never commit `.env` or API keys. Key names are listed in `.env.example`.
- Work on a branch and open a pull request. Do not push to `main`.
- Put new experiments in a dated folder under `notebooks/`, named `YYYY-MM-DD_<topic>`.
- Put reusable processing steps in `workflow/` scripts, not only in notebooks.
