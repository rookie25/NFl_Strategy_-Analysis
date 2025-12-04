# 🏈 San Francisco 49ers Offensive Strategy Analysis (2021–2024)

A comprehensive NFL play-by-play analytics project using Python & nfl_data_py.

## 📌 Project Overview

This project analyzes the San Francisco 49ers' offensive tendencies and efficiency over four seasons (2021–2024) using detailed play-by-play (PBP) data imported through the `nfl_data_py` library.

**The objectives include:**
* Offensive identity (run vs pass)
* EPA (Expected Points Added) efficiency
* Success rate trends
* Player-level impact (QBs, RBs, WR/TEs)
* Explosive plays
* Situational behavior (leading/trailing)
* Drive-level outcomes
* Red zone efficiency

This project demonstrates a complete data pipeline, exploratory analysis, feature engineering, and actionable insight generation.

## 🧰 Tools & Libraries

* **Python**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **nfl_data_py**
* **Jupyter Notebook**

## 📥 Data Source

```python
import nfl_data_py as nfl

sf = nfl.import_pbp_data([2021, 2022, 2023, 2024])
sf = sf[sf["posteam"] == "SF"].copy()
```

Dataset contains ~30,000+ offensive plays, each with 300–400+ features.

**Raw data saved in:** `raw/`  
**Processed cleaned data saved in:** `processed/`

## 📊 Key Visualizations

This repository contains eight core plots:

1. **Run vs Pass Rate**
2. **EPA by Down**
3. **Success Rate by Down**
4. **Explosive Play Rate (Run vs Pass)**
5. **Red Zone Run vs Pass**
6. **Receiver EPA per Target**
7. **RB EPA per Rush**
8. **Drive Result Distribution**

All plots include interpretations in Markdown under each plot.

## 🔍 Major Insights

### 🟥 1. Run vs Pass Identity
The 49ers maintain a balanced offense (~53% pass, ~47% run), reflecting Kyle Shanahan's adaptable system.

### 🟧 2. EPA by Down
* 2nd Down is the most efficient (+0.13 EPA)
* 3rd Down maintains strong efficiency (+0.10 EPA)
* 4th Down is naturally negative

### 🟨 3. Explosive Plays
* Pass explosive rate: ~17%
* Run explosive rate: ~9%
* The passing game drives most chunk plays (Aiyuk, Samuel, Kittle).

### 🟩 4. Red Zone Strategy
* Red zone run rate: ~54%
* Red zone pass EPA is significantly higher
* **Suggests opportunity:** more red-zone passing

### 🟦 5. Player Impact

**Quarterbacks (EPA per attempt):**
* Brock Purdy: +0.24
* Jimmy Garoppolo: +0.15
* Trey Lance: +0.04

**Running Backs:**
* McCaffrey shows highest efficiency despite heavy usage.

**Receivers:**
* Kittle and Aiyuk lead in EPA and success rate.
* Deebo Samuel produces elite YAC and explosive plays.

### 🟪 6. Drive-Level Efficiency
* Touchdown rate: 28% of drives
* Turnover rate: 11%
* Three-and-out rate: 30%
* Expected points per drive: ~1.96 (top-5 offense)

## 📁 Project Structure

```
📦 49ers_Analytics_Project
│
├── raw/
│   └── sf_raw_2021_2024.csv
│
├── processed/
│   └── sf_cleaned.csv
│
├── notebook/
│   └── 49ers_Analysis.ipynb
│
├── plots/
│   ├── run_pass_rate.png
│   ├── epa_by_down.png
│   ├── success_by_down.png
│   ├── explosive_rate.png
│   ├── redzone_rate.png
│   ├── receiver_epa.png
│   ├── rb_epa.png
│   └── drive_results.png
│
└── README.md
```

## 🚀 How to Run the Notebook

**Install dependencies:**

```bash
pip install nfl_data_py pandas matplotlib seaborn
```

**Load data in Jupyter:**

```python
import nfl_data_py as nfl
sf = nfl.import_pbp_data([2021, 2022, 2023, 2024])
```

Then follow each analysis section in `49ers_Analysis.ipynb`.

## 🎯 Future Enhancements

* 4th-down decision modeling
* EPA prediction ML model
* Win probability added (WPA) analysis
* Game-level summaries
* Drive visualization
* Player tracking integration (if available)

## 🤝 Author

**Vishal C. V.**  
MS Business Analytics | University of the Pacific  

## 🏁 Conclusion

This project provides a complete, data-driven breakdown of one of the NFL's most efficient offenses. Combining EPA, success rate, explosive plays, and player-level impact, it provides meaningful insights into how the 49ers consistently create high-value scoring opportunities.
