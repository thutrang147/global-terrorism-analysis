# Global Terrorism Database: From Chaos to Clarity
## The Power of Data Preprocessing & Unmasking the Unknown

### Course Information
**Course:** Data Preparation and Visualization - Final Project  
**Institution:** National Economics University  
**Academic Year:** 2024-2025

---

## Project Overview

This project moves beyond standard descriptive statistics to investigate the **strategic behavior** of global terrorism over nearly five decades (1970-2017). Using the **Global Terrorism Database (GTD)**, we shift the analytical focus from *"What happened?"* to *"Why is it lethal?"* and *"Who is behind the silence?"*

The analysis is structured into two critical investigations:
1. **Deconstructing the "Efficiency Paradox"** of attack tactics
2. **"Ghost Hunting"** - Profiling unknown perpetrators using Machine Learning clustering

### Dataset Characteristics
- **Source:** Global Terrorism Database (GTD) by START Consortium
- **Scope:** 181,691 incidents (1970-2017)
- **Coverage:** 205 countries, 12 regions, 135 variables
- **Key Features:** AttackType, WeaponType, Suicide, Casualties (nkill + nwound), Region, Group Name

---

## Strategic Objectives

### 1. The Efficiency Paradox
Challenge the assumption that high-frequency attacks are the most dangerous by visualizing the trade-off between **Popularity** (e.g., Bombing) and **Lethality** (e.g., Hijacking).

### 2. Anatomy of Lethality
- Dissect the **"Suicide Multiplier"** effect
- Map **"Regional Signatures"** to understand how terrain and power dynamics dictate tactical choices

### 3. "Ghost Hunting" (Clustering)
Address the critical data gap where ~50% of attacks are attributed to "Unknown" groups. We apply **K-Means Clustering** to profile these invisible actors into **5 distinct operational personas**:
- **Cluster 0:** The Agitator (Amateur/Low-level)
- **Cluster 1:** The Guerrilla
- **Cluster 2:** The Specialist (Kidnapping)
- **Cluster 3:** The Mass-Casualty Bomber
- **Cluster 4:** The Assassin

---

## Methodology

### Data Preprocessing Pipeline
1. **Contradictory Statements:** Fix logical errors (nkill < nkillus)
2. **Secret Language of Missing Values:** Standardize error codes (-9, -99, NaN)
3. **Forgotten Cases:** Remove columns with >90% missing values
4. **Case Studies:** Clean specific columns (nperps, nhostkid)

### Machine Learning Approach
- **Technique:** MiniBatchKMeans with PCA dimensionality reduction
- **Preprocessing:** Winsorization, Log transformation, Quantile normalization
- **Encoding:** Frequency encoding for categorical features, One-hot encoding
- **Validation:** Silhouette analysis and cluster interpretation

### Visualization Strategy
- **Treemap:** Cluster volume comparison
- **Horizontal Stacked Bar:** Lethality analysis (killed + wounded)
- **100% Stacked Bar:** Tactical fingerprint (attack type distribution)
- **Area Chart:** Success rate comparison

---

## Team Contributions

| Team Member | Student ID | Contribution |
|------------|-----------|--------------|
| **Vu Ngoc Hong Anh (Leader)** | 11230517 | 20% |
| **Nguyen Thi Thu Trang** | 11230595 |  20% |
| **Tran Tuan Anh** | 11230515 | 20% |
| **Nguyen Phuong Dong** | 11230530 | 20% |
| **Nguyen Vinh Khanh** | 11230549 | 20% |

---

## Folder Structure

```
GlobalTerrorism/
├── data/
│   ├── globalterrorismdb.csv
│   └── ne_110m_admin_0_countries.*  # Natural Earth shapefile components
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
   - **On macOS/Linux:**  
     ```
     source .venv/bin/activate
     ```
   - **On Windows (Command Prompt):**  
     ```
     .venv\Scripts\activate
     ```
   - **On Windows (PowerShell):**  
     ```
     .venv\Scripts\Activate.ps1
     ```

3. **Install dependencies:**  
   ```
   pip install -r requirements.txt
   ```

4. **Download the data:**  
   - Download the main dataset:  
     [Global Terrorism Database Download Page](https://www.start.umd.edu/gtd-download)  
     Place `globalterrorismdb.csv` in the `data/` folder.
   - Download the world countries shapefile (Natural Earth):  
     [ne_110m_admin_0_countries.zip](https://www.naturalearthdata.com/downloads/110m-cultural-vectors/110m-admin-0-countries/)  
     Unzip and place all files (e.g., `.shp`, `.shx`, `.dbf`, etc.) into the `data/` folder.

5. **Run the notebook:**  
   Open `main.ipynb` in Jupyter or VSCode and execute the cells in order.

> **Tip:** In VS Code, use the command palette to select the Python interpreter from `.venv` for best compatibility.

## References

- [Global Terrorism Database (START, University of Maryland)](https://www.start.umd.edu/gtd/)
- Variable descriptions: see the notebook for a detailed data dictionary.