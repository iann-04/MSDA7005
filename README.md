# MSDA7005 · Upworthy headline analysis

This project examines the association between negative wording and headline click-through rates, and whether the association varies with linguistic complexity.

## Run the notebooks

Install the Python dependencies with `python -m pip install -r requirements.txt`. Start JupyterLab in this directory with `jupyter lab`.

1. Download the **NRC Emotion Lexicon v0.92** from the [official resource page](https://www.saifmohammad.com/WebPages/AccessResource.htm). Extract `NRC-emotion-lexicon-wordlevel-alphabetized-v0.92.txt` next to the notebooks. The lexicon's terms restrict redistribution. Extract `regression_df_update_06122024.csv.zip` in the same directory to obtain the original Upworthy CSV.
2. Run `01_data_processing.ipynb` to clean and score the headlines.
3. Run `02_rq1.ipynb` for the main association, within-experiment comparison, and exploratory contrasts.
4. Run `03_rq2.ipynb` for the interaction, within-experiment comparison, and scoring sensitivity analysis.

The notebooks use `7005_notebook_outputs/` by default. It contains the scored dataset, result tables, and figures, so the two analysis notebooks can also start from the committed scored data. Set `UPWORTHY_DATA_DIR` or `UPWORTHY_RUN_DIR` to point to another input or output directory.

For RQ2, use the experiment-clustered columns in the CSVs for inference. The ordinary-SE sensitivity figure highlights selected specifications. The full three-rule comparison is in `RQ2_all_alternative_scoring.csv`.

## Data sources

- [Upworthy study data and replication materials](https://osf.io/uscpf/).
- [NRC Emotion Lexicon, Mohammad and Turney](https://www.saifmohammad.com/WebPages/AccessResource.htm).

