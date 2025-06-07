# STATISTICAL-ANALYSIS-Using-R

A collection of statistical analysis projects implemented in **R** (via Jupyter notebooks). This repository contains all data, code, and visual assets used across five individual projects, plus a set of “useful code” snippets for common statistical tasks.

---

## 📂 Repository Structure

```

STATISTICAL-ANALYSIS-R/
│
├── Data/
│   └── Data.rar
│
├── Projects/
│   ├── Images/
│   │   └── (figures, plots, and other image assets used in notebooks)
│   │
│   ├── Project\_1.ipynb    # Exploratory Data Analysis on \[Dataset A]
│   ├── Project\_2.ipynb    # Regression Modeling of \[Dataset B]
│   ├── Project\_3.ipynb    # Time Series Forecasting of \[Series C]
│   ├── Project\_4.ipynb    # Classification Analysis on \[Dataset D]
│   └── Project\_5.ipynb    # Clustering & Dimensionality Reduction on \[Dataset E]
│
└── Useful-Codes/
├── data\_cleaning.R    # Common data wrangling functions
├── plotting\_utils.R   # ggplot2 wrappers and themes
└── stats\_helpers.R    # Functions for hypothesis testing, effect sizes, etc.

````

---

## 🚀 Getting Started

### 1. Prerequisites

- **R** (version ≥ 4.0)  
- **Jupyter Notebook** or **JupyterLab**  
- **IRkernel** installed & registered with Jupyter:  
  ```bash
  R -e "install.packages('IRkernel'); IRkernel::installspec()"
````

* R packages commonly used across projects (install all at once):

  ```r
  install.packages(c(
    'tidyverse', 'data.table', 'ggplot2', 'forecast',
    'caret', 'cluster', 'factoextra', 'broom'
  ))
  ```

### 2. Downloading the Data

All raw data sets are bundled into a single compressed archive:

```bash
cd STATISTICAL-ANALYSIS-R/Data
unrar x Data.rar
```

> **Note:** If you don’t have `unrar`, you can install it via your package manager (e.g. `sudo apt install unrar` on Ubuntu).

Unpacking will create one or more `.csv` (or other) files that each notebook expects in its working directory.

### 3. Running the Notebooks

1. Navigate back to the root of the repo:

   ```bash
   cd ../..
   ```
2. Launch Jupyter:

   ```bash
   jupyter lab
   ```
3. Open any `Project_X.ipynb` under `Projects/` and make sure the **R** kernel is selected.
4. Execute cells sequentially.

   * Data import steps assume the extracted files remain in `Data/`.
   * Image outputs (plots, charts) will write to `Projects/Images/` when the code calls `ggsave()` or similar.

---

## 📘 Project Overviews

Below is a brief description of each project’s goals and techniques:

| Notebook       | Focus Area                                     | Key Techniques                                  |
| -------------- | ---------------------------------------------- | ----------------------------------------------- |
| **Project\_1** | Exploratory Data Analysis on **Dataset A**     | Summary statistics, ggplot2 visualizations      |
| **Project\_2** | Regression Modeling of **Dataset B**           | Linear & multiple regression, diagnostics       |
| **Project\_3** | Time Series Forecasting of **Series C**        | ARIMA modeling, decomposition, forecast plots   |
| **Project\_4** | Classification Analysis on **Dataset D**       | Logistic regression, decision trees, ROC curves |
| **Project\_5** | Clustering & Dimensionality Reduction on **E** | K-means, hierarchical clustering, PCA           |

*(Replace **Dataset A–E** with actual dataset names if desired.)*

---

## 🧰 Useful-Codes

Inside `Useful-Codes/`, you’ll find R scripts that define reusable functions:

* **`data_cleaning.R`**
  Functions for handling missing values, recoding factors, outlier removal, etc.

* **`plotting_utils.R`**
  Pre-configured ggplot2 themes, custom color palettes, and helper wrappers.

* **`stats_helpers.R`**
  Convenience functions for t-tests, ANOVA summaries, effect-size calculations.

To use these in a notebook:

```r
source("../Useful-Codes/data_cleaning.R")
source("../Useful-Codes/plotting_utils.R")
source("../Useful-Codes/stats_helpers.R")
```

---

## 📜 License & Citation

This work is licensed under the [MIT License](LICENSE).
If you use or build upon these analyses, please cite:

> *Your Name*, *Statistical Analysis in R*, GitHub Repository, Year.

---

## ✉️ Contact

For questions, feature requests, or additional datasets, open an issue or contact me at **[saeedrafsharx@gmail.com](mailto:saeedrafsharx@gmail.com)**.

Happy analyzing! 📊🚀
