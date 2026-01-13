# Wellbeing Prediction Output Visualisation & Aggregation

This repository focuses on visualising and aggregating outputs from the wellbeing prediction model. Jupyter notebooks explore yearly CSV predictions and generate plots and summary tables that can be exported to `outputs/`.

## Project Structure

- `probability_visualisation_*.ipynb` — visualisation notebooks per dataset/code.
- `aggregation_thresholds.ipynb` — aggregation outputs and threshold summaries.
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
- Start the relevant notebook: `jupyter notebook probability_visualisation_FPH.ipynb`.
- Run cells in order to refresh plots or aggregation summaries; save exports to `outputs/` to keep the working directory clean.
