# Global Terrorism Database Analysis

## Project Overview

This project analyzes nearly five decades of global terrorism data (1970–2017) from the **Global Terrorism Database (GTD)**, maintained by the START Consortium at the University of Maryland. The GTD is the most comprehensive unclassified database on terrorist events worldwide, containing detailed information on over 181,000 attacks.

### Objectives

- **Temporal Analysis:** Identify patterns, trends, and turning points in terrorist activity over 48 years.
- **Geographic Mapping:** Visualize regional concentrations and country-level hotspots.
- **Tactical Evolution:** Analyze attack methods, weaponry, and target selection patterns.
- **Actor Profiling:** Use machine learning to cluster unknown perpetrators and analyze group longevity.
- **Human Impact:** Quantify casualties, hostage situations, and victim demographics.

## Features

- **Data Cleaning:** Handle missing values, remove incomplete years, engineer features.
- **Visualization:** Professional dashboards using Matplotlib, Seaborn, Plotly.
- **Machine Learning:** PCA + KMeans clustering for perpetrator profiling.
- **Statistical Analysis:** Temporal aggregations, geographic distributions, and correlation studies.
- **In-depth Analysis:** Compare Muslim-majority and Western regions, analyze group dynamics, and hostage situations.

## Folder Structure

```
GlobalTerrorism/
├── data/
│   └── globalterrorismdb.csv
├── main.ipynb
├── README.md
└── requirements.txt
```

## How to Use

1. **Create a virtual environment:**  
   Open your terminal and run:
   ```
   python3 -m venv .venv
   ```

2. **Activate the virtual environment:**  
   ```
   source .venv/bin/activate
   ```

3. **Install dependencies:**  
   ```
   pip install -r requirements.txt
   ```

4. **Run the notebook:**  
   Open `main.ipynb` in Jupyter or VSCode and execute the cells in order.

5. **Data:**  
   Place `globalterrorismdb.csv` in the `data/` folder.

> **Tip:** In VS Code, use the command palette to select the Python interpreter from `.venv` for best compatibility.

## References

- [Global Terrorism Database (START, University of Maryland)](https://www.start.umd.edu/gtd/)
- Variable descriptions: see the notebook for a detailed data dictionary.