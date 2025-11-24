# Wellbeing BERT Result Visualisation

This repository holds a Jupyter notebook for exploring yearly wellbeing prediction outputs from a BERT model. Raw CSV predictions live locally under `data/`, and the notebook produces plots that can be exported to `outputs/`.

## Project Structure
- `probability_visualisation.ipynb` — main analysis and plotting notebook.
- `data/` — yearly prediction CSVs (`preds-FPHYYYY.csv`, not tracked by git).
- `outputs/` — optional notebook exports (HTML, PNGs), also ignored by git.

## Setup
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install pandas matplotlib seaborn jupyter
```

## Usage
- Place input files in `data/` using the naming pattern `preds-FPHYYYY.csv`.
- Start the notebook: `jupyter notebook probability_visualisation.ipynb`.
- Run cells in order to refresh plots; save exports to `outputs/` to keep the working directory clean.

## Contributing Notes
- Follow PEP 8 in any added Python scripts.
- Keep AGENTS.md for local guidance only; it is intentionally ignored by git.
- If you add scripts, place them in `scripts/` and add brief in-notebook notes describing their purpose.
