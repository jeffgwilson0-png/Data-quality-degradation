# Predicting model degradation from data defects before training

Code and result files for the paper *Adaptive Data Quality Assessment for Machine Learning Pipelines: Predicting Model Degradation Before Training* (J. G. Wilson, K. Makadiya).

A random forest meta-model predicts how much accuracy a model loses because of data defects (label noise, missing values, duplicates, class imbalance) from cheap meta-features of the damaged training set. It is evaluated on 48 OpenML-CC18 datasets.

## Contents

| Folder | What is in it |
|---|---|
| `notebooks/` | Google Colab notebooks, numbered in the order they were created. `4_extended_experiment` is the extended experiment (5 models, 3 measures, class-dependent noise); `5_reviewer_experiments` answers the reviewers (10 seeds, cleanlab, timing, ranking test, instance-dependent noise). |
| `results/` | The `result*.csv` tables produced by the notebooks (add them from your Drive folders `data_quality_paper_extended` and `data_quality_paper_v7`). |
| `paper/` | LaTeX source of the submitted paper. |

## How to run

1. Open a notebook in Google Colab and run the cells from the top. Results are saved to Google Drive after every dataset and seed, so a stopped run can be continued.
2. Notebook 5 re-uses the files written by notebook 4 and adds seeds 3-9. Set `FAST_TEST = True` first for a quick check.
3. Datasets are downloaded from OpenML (OpenML-CC18). The dataset IDs are listed in the notebooks.

Python packages: see `requirements.txt`.

## License

MIT, see `LICENSE`.
