# Hull-Tactical

Quantitative trading research and experimentation repository focused on the **Hull Tactical** strategy family.  
This project is structured primarily as a collection of Jupyter notebooks, with light Python support code.

> **Note**  
> This repository is intended for research, prototyping, and education. It is **not** investment advice and is **not** a production trading system.

---

## Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Running the Notebooks](#running-the-notebooks)
  - [Configuration](#configuration)
- [Data](#data)
- [Project Goals](#project-goals)
- [Contributing](#contributing)
- [License](#license)
- [Disclaimer](#disclaimer)

---

## Overview

The **Hull-Tactical** repository is a research sandbox for exploring:

- Tactical asset allocation and timing rules inspired by Hull-style strategies
- Signal construction and feature engineering
- Backtesting and performance evaluation
- Risk management and position sizing approaches

Because the repository is almost entirely composed of Jupyter notebooks (≈99.7%), it is designed to be:

- **Interactive** – tweak parameters and re-run cells to see immediate impact
- **Exploratory** – compare multiple variants of rules or indicators
- **Documented-by-example** – most explanations live directly alongside the code and output in notebooks

---

## Repository Structure

> This is a generic structure; adapt the folder and file names to your actual layout.

```text
Hull-Tactical/
├─ notebooks/
│  ├─ 01_data_exploration.ipynb
│  ├─ 02_signal_construction.ipynb
│  ├─ 03_backtest_hull_tactical.ipynb
│  └─ 99_experiments_scratchpad.ipynb
├─ src/                    # (Optional) helper Python modules
│  ├─ data_loader.py
│  ├─ backtester.py
│  └─ utils.py
├─ requirements.txt        # Python dependencies
├─ environment.yml         # (Optional) conda environment
└─ README.md
```

- **`notebooks/`** – main research notebooks, ordered roughly by workflow stage.
- **`src/`** – small Python helpers used by notebooks for data loading, backtesting, and utilities.
- **`requirements.txt` / `environment.yml`** – reproducible environment definitions.

---

## Getting Started

### Prerequisites

- **Python**: 3.9+ (3.11 recommended)
- **Package manager**: `pip` or `conda`
- **Jupyter**:
  - [JupyterLab](https://jupyter.org/) or
  - Classic Jupyter Notebook

### Installation

Clone the repository:

```bash
git clone https://github.com/Shenzhen-shoegazer/Hull-Tactical.git
cd Hull-Tactical
```

Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
source .venv/bin/activate      # On Windows: .venv\Scripts\activate
```

Install dependencies using `pip`:

```bash
pip install -r requirements.txt
```

Or, if you prefer `conda` and an `environment.yml` file is provided:

```bash
conda env create -f environment.yml
conda activate hull-tactical
```

---

## Usage

### Running the Notebooks

From the project root:

```bash
jupyter lab
# or
jupyter notebook
```

Then open any notebook in the `notebooks/` directory, for example:

- `01_data_exploration.ipynb`
- `02_signal_construction.ipynb`
- `03_backtest_hull_tactical.ipynb`

Run the cells top-to-bottom. Many notebooks are parameterized via variables at the top (e.g., tickers, lookback windows, rebalance frequency) so you can quickly adjust and re-run.

### Configuration

Depending on how the project is set up, configuration may be handled via:

- **Environment variables** (e.g. `DATA_DIR`, API keys)
- **YAML/JSON config files** in `config/`
- **Hard-coded paths** at the top of each notebook (common in early research)

Check the first few cells of each notebook for instructions on:

- Where to store or download raw data
- What tickers, indices, or asset classes are used
- Date ranges and frequency (daily, weekly, etc.)

---

## Data

This repository does **not** distribute proprietary market data.

Typical data sources (you may need accounts / API keys):

- CSV files from your own data vendor
- Public data via APIs (e.g., Yahoo Finance, FRED) accessed in notebooks
- Local files under a directory such as `data/` (ignored by Git if large or proprietary)

> Ensure that you comply with the **license and terms of use** of any data provider you integrate with.

---

## Project Goals

This repository is intended to support:

1. **Strategy research**  
   - Investigate Hull-style and related tactical allocation signals
   - Compare rules-based vs. indicator-based timing approaches

2. **Backtesting & evaluation**  
   - Evaluate strategy performance vs. benchmarks
   - Analyze drawdowns, volatility, and risk-adjusted metrics

3. **Robustness checks**  
   - Parameter sensitivity studies
   - Regime analysis (e.g., bull vs. bear markets)

4. **Education & documentation**  
   - Demonstrate a clear, notebook-driven research workflow
   - Serve as a reference for future strategy development

---

## Contributing

Contributions, ideas, and discussion are welcome.

### How to contribute

1. **Fork** the repository
2. Create a new **branch** for your feature or experiment:
   ```bash
   git checkout -b feature/my-experiment
   ```
3. Make changes in notebooks or `src/` utilities
4. Run notebooks top-to-bottom to ensure they execute cleanly
5. Commit with a clear message and push your branch
6. Open a **Pull Request** with:
   - A concise description of what you changed
   - Any references or rationale for new tactics or indicators

Before contributing, please:

- Avoid committing large raw data files or credentials
- Keep notebooks reasonably clean (remove unrelated scratch code and large outputs when possible)

---

## License

Specify your chosen license here, for example:

This project is licensed under the **MIT License** – see the [`LICENSE`](LICENSE) file for details.

If no license file exists yet, please add one before sharing or collaborating widely.

---

## Disclaimer

This repository is for **research and educational purposes only**.

- Nothing in this project constitutes financial, investment, trading, or other professional advice.
- Past performance of strategies described or backtested here is **not** indicative of future results.
- Use any code, ideas, or results at your own risk.

By using this repository, you agree that the author(s) and contributors are **not liable** for any losses, damages, or other consequences arising from its use.