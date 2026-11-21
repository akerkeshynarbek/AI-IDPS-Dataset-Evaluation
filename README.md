# AI-Based Intrusion Detection: Reproducibility Package (DRAFT)

This package contains **sanitized, unexecuted copies** of the researcher's CICIDS2017 and UNSW-NB15 Colab notebooks. Original notebooks should be retained privately as archival records.

**Status:** Draft for researcher review. The sanitized notebooks have **not** been executed end-to-end. This package does **not** contain datasets, trained models, final exported CSVs, or a verified environment lockfile. Do not describe it as a fully reproduced experiment or publish it before review.

## Contents

- `notebooks/CICIDS2017_experiments_clean.ipynb` — CICIDS2017 audit and model experiments (72 code/markdown cells in source).
- `notebooks/UNSW_NB15_experiments_clean.ipynb` — UNSW-NB15 audit and final official-test experiments.
- `requirements.txt` — broad dependencies only; not an exact environment lock.
- `.gitignore` — excludes datasets, outputs, credentials and large files.
- `DATA_AVAILABILITY.md` — conservative manuscript statement and release checklist.

## Obtain the datasets

Download CICIDS2017 and UNSW-NB15 from their **official dataset providers**, following their usage conditions. Do not commit the original datasets into this repository.

- CICIDS2017: put the original MachineLearningCVE CSV files in `data/CICIDS2017/MachineLearningCSV/` or edit `data_folder` in the first notebook cell.
- UNSW-NB15: put `UNSW_NB15_training-set.csv` and `UNSW_NB15_testing-set.csv` in the notebook working directory, or change the read paths in its first loading cell.

The CICIDS2017 notebook saves intermediate files under `data_folder.parent/experimentXX/`. The portable input path has **not been tested end-to-end**. The UNSW notebook expects the official CSV files in its working directory; upload them through the Colab Files panel or supply local files.

## Reproduction guidance

1. Create a Python environment and install `requirements.txt`.
2. Download the exact input CSV releases.
3. Adjust dataset paths and execute cells **in order**; some later experiments depend on files created by earlier cells.
4. Record package versions, CPU/RAM, notebook runtime, data file hashes, and final confusion matrices.
5. Compare produced metrics with the published article; investigate any mismatch.

## Publication checklist

- [ ] Check every code and Markdown cell for identifying information and private paths.
- [ ] Verify no API tokens, credentials, embedded data, or private URLs remain.
- [ ] Run both cleaned notebooks from a fresh environment with official datasets.
- [ ] Export the UNSW-NB15 exact confusion matrix and final result tables.
- [ ] Add environment versions and hardware details from the actual run.
- [ ] Decide whether to license the code and choose a suitable license.
- [ ] Confirm university/journal permissions and publication timing.
- [ ] Create a public repository **only when ready**, then archive a versioned release on Zenodo if desired.
