# Repository Guidelines

## Project Structure & Assets
- Core analysis lives in the notebook `probability_visualisation.ipynb`.
- Input predictions are yearly CSVs under `data/` (`preds-FPHYYYY.csv`). Keep the naming pattern for new drops.
- No Python modules are present; if you add scripts, place them in `scripts/` and keep data outputs in `data/` or `outputs/`.

## Environment Setup & Dev Commands
- Create an isolated environment: `python3 -m venv .venv && source .venv/bin/activate`.
- Install essentials: `pip install pandas matplotlib seaborn jupyter`.
- Launch the notebook locally: `jupyter notebook probability_visualisation.ipynb`.
- Optional: export a static run with `jupyter nbconvert --to html probability_visualisation.ipynb`.

## Running & Visualising
- Ensure all `data/preds-FPHYYYY.csv` files you need are present; columns should match the existing ones used in the notebook.
- Execute cells in order; re-run the full notebook after changing inputs to regenerate plots consistently.
- If you add derived assets (plots, tables), write them to `outputs/` and avoid overwriting raw inputs.

## Coding Style & Naming Conventions
- Follow PEP 8 in any added Python: 4-space indentation, `snake_case` functions/variables, `CamelCase` classes.
- Prefer explicit imports (`import pandas as pd`, `import matplotlib.pyplot as plt`, `import seaborn as sns`), mirroring the notebook.
- Keep notebook cells focused; extract reusable logic into helper functions if it grows.

## Testing Expectations
- There are no automated tests yet; when adding Python modules, include `pytest` tests under `tests/` and name files `test_*.py`.
- For notebooks, add sanity checks (assertions on column presence/shapes) near data loading to catch schema changes early.
- If plots are key outputs, keep sample CSVs in `data/` and document expected shapes to make manual verification quick.

## Commit & Pull Request Guidelines
- Use concise commit subjects in the imperative mood (e.g., `Add sanity checks for FPH data`, `Refine seaborn plot styles`); group related notebook changes together.
- PRs should summarize intent, note data sources/versions touched, and include before/after visuals for plot changes when feasible.
- Link any tracking ticket or issue, and list manual verification steps (e.g., notebook cells executed, outputs inspected).

## Security & Data Handling
- Do not commit sensitive or proprietary data; keep raw inputs in `data/` but consider `.gitignore` if adding local-only files.
- Document any new data schema or transformations directly in the notebook or a short README snippet near the added script.
