# MSDA7005 · Upworthy headline analysis

We use Upworthy A/B test data to study how negative wording relates to headline click-through rates and whether that relationship varies with linguistic complexity.

## Run

1. Install the Python dependencies with `python -m pip install -r requirements.txt`.
2. Extract `regression_df_update_06122024.csv.zip` next to the notebooks. Download [NRC Emotion Lexicon v0.92](https://www.saifmohammad.com/WebPages/AccessResource.htm) from the official source and place the word-level file beside the notebooks as `NRC-emotion-lexicon-wordlevel-alphabetized-v0.92.txt`.
3. Start Jupyter Notebook with `jupyter notebook`, then run all cells in order in `01_data_processing.ipynb`, `02_rq1.ipynb`, and `03_rq2.ipynb`.

The default output directory is `7005_notebook_outputs/`. To run just RQ1 or RQ2, extract the committed `upworthy_v2_scored.csv.zip` in that directory first. Use `UPWORTHY_DATA_DIR` and `UPWORTHY_RUN_DIR` to change the input and output locations. Choose an empty output directory for a fresh run.

## Figures and tables

| Notebook | PPT figures | CSVs |
| --- | --- | --- |
| 01 Data processing | A/B test sizes and the negative-word distribution. The example headline pair appears as a table inside the notebook. | Scored headlines for both research questions |
| 02 RQ1 | Predicted CTR, within-experiment comparison, and the exploratory presence/dose comparison | M1 regression and exploratory contrasts |
| 03 RQ2 | Four-point comparison, scoring sensitivity, and observed negative-word shares by Fog group | M2 regression, all three scoring variants, and predicted click contrasts |

The four-point and selected scoring plots label ordinary model-based intervals to match the presentation. The RQ2 CSVs also report experiment-clustered intervals. For the main interaction and change in gains between low and high Fog, the clustered intervals span zero.

[Upworthy study data and replication materials](https://osf.io/uscpf/)

