# Project name

One or two sentences on what this project studies and why.

> **Setting up a new repo from this template?** Work through [Using this template](#using-this-template) at the bottom, then delete that section.

## Repository layout

1. `data/` for raw and derived datasets. See `data/README.md` for what to commit and how to document each dataset.
1. `libs/` for the project's reusable Python package, installed in editable mode.
1. `notebooks/` for dated experiment notebooks.
1. `workflow/` for data processing and analysis scripts, ideally run through Snakemake.
1. `AGENTS.md` for instructions to AI coding agents. `CLAUDE.md` imports it.
1. `.gitignore` for Python, Jupyter, macOS, Snakemake, secrets, and derived data files.
1. `.env.example` for the names of the API keys the project needs.

## Setup

This project uses [uv](https://docs.astral.sh/uv/) to manage Python and dependencies.

```bash
uv sync                  # create .venv and install dependencies, including libs/ in editable mode
cp .env.example .env     # then fill in your own API keys; .env is git-ignored
uv run jupyter lab       # start Jupyter inside the project environment
uv run snakemake -j 1    # run the pipeline in workflow/
```

Add a dependency with `uv add <package>`. Commit both `pyproject.toml` and `uv.lock`.

## Logistics

- **Project management:** tasks live in GitHub Issues and the project's GitHub Project board.
- **Lab practices:** the [lab manual](https://github.com/YangKCLab/lab-manual) (lab members only) covers research practices, reproducibility, data sharing, and human-subjects research.
- **Committing new code:** create a new [branch](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches), then open a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests). At least one reviewer signs off before a merge to `main`.

## Using this template

GitHub copies only the files of a template. It does not copy branch protection, labels, or project boards. After creating a repo from this template:

- [ ] Replace "Project name" and the description at the top of this README.
- [ ] Rename the package: rename `libs/project_package_name/`, and update the name in `libs/pyproject.toml` and in the root `pyproject.toml` (`dependencies` and `[tool.uv.sources]`). Also set the root project `name` and `description`.
- [ ] Run `uv sync` and commit the generated `uv.lock`.
- [ ] Fill in `AGENTS.md`.
- [ ] Protect `main` so changes go through reviewed pull requests: **Settings → Rules → Rulesets**, or **Settings → Branches** → add a rule for `main` that requires a pull request with one approval.
- [ ] Delete this section.
