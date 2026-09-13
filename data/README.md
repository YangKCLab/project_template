This is the folder for storing raw and derived datasets.
Do not commit large datasets to the git repository.

The folder follows the [Cookiecutter Data Science](https://cookiecutter-data-science.drivendata.org/) layout:

```
├── data
│   ├── external       <- Data from third-party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical datasets for analysis.
│   └── raw            <- The original, immutable data dump.
```

`.gitignore` ignores the contents of `external/`, `interim/`, and `processed/` by default. Each folder keeps a `.gitkeep` file so the folder exists in a fresh clone. `raw/` is tracked.

Follow one of these practices:

1. If the raw data is small and not sensitive, commit it to `raw/`. Keep derived datasets local.
1. Large and sensitive files stay on remote servers or in the lab's shared storage. Add their paths under `raw/` to `.gitignore`.
1. If the dataset has a fixed location (URL), add a download step to the workflow. Git-ignore the downloaded and derived files.

Whenever possible, make the raw data files **read-only**.

## Sensitive data and data sharing

- The lab expects non-sensitive data to be made public when the paper is published, with enough documentation for others to replicate the analysis. Sharing plans for sensitive data are decided case by case. See "Reproducibility" in [research practices](https://github.com/YangKCLab/lab-manual/blob/main/docs/research-practices.md) (lab members only).
- Data about people may need IRB review before you collect or analyze it. Read [human subject research](https://github.com/YangKCLab/lab-manual/blob/main/docs/human-subject-research.md) (lab members only) before you start, and talk to Kaicheng if you are unsure.
- Never commit API keys, passwords, or personal identifiers. Keys go in `.env`, which is git-ignored.

## Data documentation

Update this document with detailed documentation (a data dictionary) for each dataset. Document at least the following, and ideally write a [datasheet](https://arxiv.org/abs/1803.09010):

1. _When_ was the data obtained?
2. _From whom_ or _where_ did you get the data?
3. What does each column mean? What is the _data format_ of each column? Loading a column with a wrong assumption about its format can cost your project.
4. What other information, restrictions, and limitations apply to the dataset? How was the data collected? What biases does it contain? What should not be done with it (for example, identifying individuals)?
