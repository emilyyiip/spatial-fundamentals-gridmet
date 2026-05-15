# gridMET Foundations: Working with Spatial Meteorological Data

This repository contains a self-contained Jupyter notebook that teaches the
foundational concepts of working with spatial meteorological data using gridMET
NetCDF files. It is designed for researchers who have basic
Python experience but no prior exposure to geographic or spatial data.

---

## What You Will Learn

- What gridMET is and how to download data from it programmatically
- How NetCDF files are structured (dimensions, variables, coordinates, attributes)
- What spatial resolution means and how to visualize a data grid
- What temporal resolution means and how to work with daily time series
- How to make maps of gridded data
- What a Coordinate Reference System (CRS) is and why it matters
- How to aggregate gridded data to administrative units (parishes)

---

## Prerequisites

- Python 3.9 or higher
- Conda (Anaconda or Miniconda) installed
- Basic familiarity with Python and Jupyter notebooks

---

## Setup Instructions

### 1. Clone the repository

```
git clone https://github.com/arnabkdey/spatial-fundamentals-gridmet.git
cd spatial-fundamentals-gridmet
```

### 2. Create the conda environment

This command creates a new conda environment with all required packages.
Run it from the repository root directory.

```
conda create -n gridmet-learn python=3.11 --file requirements.txt -c conda-forge -y
```

### 3. Activate the environment

```
conda activate gridmet-learn
```

### 4. Launch Jupyter

```
jupyter notebook
```

### 5. Open the notebook

In the Jupyter file browser, navigate to `notebooks/` and open
`gridmet_foundations.ipynb`.

---

## How to Use the Notebook

Run all code cells from top to bottom in order. Do not skip cells or run them
out of order -- each cell builds on variables created in the cells above it.

The notebook will automatically download a small (~4 MB) subset of gridMET
data for Louisiana. An internet connection is required the first time you run
Section 1.

Each section ends with reflection questions. Type your answers directly into
the markdown cell below the questions -- double-click the cell to edit it.

---

## Data

The notebook downloads maximum temperature data from the gridMET dataset
(Abatzoglou 2013) via the THREDDS OPeNDAP server at Northwest Knowledge
Network. Parish boundary shapefiles are downloaded from the US Census Bureau
TIGER/Line repository. No data files need to be downloaded manually.

Downloaded data files are saved to the `data/` directory and are excluded
from version control via `.gitignore`.
