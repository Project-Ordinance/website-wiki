# Project Ordinance Wiki (MkDocs Material)

A ready-to-run, easily configurable wiki for Project Ordinance. Content is Markdown; data-driven sections (Team, Characters, Maps) pull from simple YAML files.

## Quick start

```bash
# 1) (optional) create and activate a virtualenv
python -m venv .venv
# Windows
.\.venv\Scripts\activate
# macOS/Linux
# source .venv/bin/activate

# 2) install deps
pip install -r requirements.txt

# 3) run the dev server
mkdocs serve
# then open http://127.0.0.1:8000/
```

## Edit content

- Markdown pages live under `docs/`.
- Data lives in `docs/data/`:
  - `team.yml` — list of team members
  - `characters.yml` — character registry
  - `maps.yml` — map tiles / info

The pages `team/index.md`, `characters/index.md`, and `maps/index.md` render from those YAML files using macros.

## Deploy (GitHub Pages)

Push this repository to GitHub and enable Pages. Or use the included workflow:

- Edit `.github/workflows/deploy.yml` and set your repository name (if needed).
- On push to `main`, the site builds and deploys automatically.

## Import characters from CSV

Use `tools/import_characters_csv.py` to convert a CSV (with headers) into `docs/data/characters.yml`.
