# ETL Pipeline — COVID-19 Brazil

This repository contains an ETL (Extract, Transform, Load) pipeline implemented as a Jupyter/Colab notebook. The pipeline extracts public COVID-19 data, transforms it by keeping the important fields and filtering only Brazil records, and loads the result into a file-based dataset for further analysis.

Table of contents
- [About](#about)
- [Repository structure](#repository-structure)
- [Prerequisites](#prerequisites)
- [How to run](#how-to-run)
- [Data sources](#data-sources)
- [Output](#output)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

About

The core of this project is a single Jupyter notebook (pipeline.ipynb) that demonstrates an end-to-end ETL workflow for COVID-19 data focused on Brazil. It's suitable to run on Google Colab or on a local Jupyter environment.

Repository structure

- pipeline.ipynb  — main Colab/Jupyter notebook containing the ETL implementation

Prerequisites

- Python 3.8+ (for local execution)
- Jupyter or Google Colab to run the notebook
- Typical Python libraries used in notebooks: `pandas`, `requests`, `numpy`. See the notebook for the exact dependency list.

How to run

Option A — Run in Google Colab (recommended for quick start):
1. Open `pipeline.ipynb` in Colab: https://colab.research.google.com/github/Guilherme23645/etl-pipeline/blob/main/pipeline.ipynb
2. Run the cells from top to bottom. Provide any required credentials or file paths if prompted.

Option B — Run locally:
1. Clone the repository:

```bash
git clone https://github.com/Guilherme23645/etl-pipeline.git
cd etl-pipeline
```

2. (Optional) Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate  # macOS / Linux
.venv\Scripts\activate     # Windows
```

3. Install commonly required packages (refer to the notebook for exact requirements):

```bash
pip install pandas requests jupyterlab
```

4. Start Jupyter and open `pipeline.ipynb`:

```bash
jupyter lab
```

Data sources

The notebook downloads COVID-19 data from public datasets. For the exact data source URLs (for example, Our World in Data or Johns Hopkins datasets) check the cells in `pipeline.ipynb` which contain the download/extraction steps.

Output

After running the pipeline the notebook saves the processed Brazil-only dataset to disk (CSV/Parquet or another file format depending on the notebook code). Check the final cells in `pipeline.ipynb` to find the exact output path(s).

Contributing

Contributions are welcome. If you'd like to add features or improve the pipeline, please open an issue or submit a pull request. Keep changes focused and include tests or example outputs when appropriate.

Contact

Maintainer: Guilherme Henrique de Paula (<gui.depaula236@gmail.com>)

Notes

- The notebook is the source of truth for the implementation details. This README provides a quick overview and instructions for running the notebook.
