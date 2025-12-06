# ❄️ Data Slayers - Frost Risk Forecasting Data Challenge

This repository contains our team's work for the F3 frost risk forecast data challenge, hosted by UC San Diego and the National Data Platform (NDP). 

Our goal was to develop a machine learning model to accurately predict frost occurrences 3, 6, 12, 24 hours ahead using meteorological, environmental, and temporal features, and compare these predictions to baseline heuristics. 

---

## 📁 Repository Structure
```
├── cimis-hourly-data-multiple-stations/	# Hourly station data     
├── plots/  # Station plots and graphs
├── .gitignore  # Git ignore config
├── baseline.ipynb  # Traditional heuristic notebook
├── f3_data_challenge_main.ipynb  # Final pipeline notebook 
├── README.md  # This file 
├── requirements.txt  # Required Python packages
```
---

## 📊 Dataset

**CIMIS Hourly Data - Multiple Stations**

Provided by the California Irrigation Management Information System (CIMIS), this dataset includes hourly meteorological measurements from 2010-2025 for 18 different weather stations within California. Data files:

- `2-fivepoints.csv`
- `7-firebaugh.csv`
- `15-stratford.csv`
- `39-parlier.csv`
- `47-brentwood.csv`
- `70-manteca.csv`
- `71-modesto.csv`
- `80-fresnostate.csv`
- `105-westlands.csv`
- `124-panoche.csv`
- `125-arvinedison.csv`
- `131-fairoaks.csv`
- `146-belridge.csv`
- `182-delano.csv`
- `194-oakdale.csv`
- `195-auburn.csv`
- `205-coalinga.csv`
- `206-denairii.csv`
- `cimis_all_stations.csv.gz`

---

## 💭 Modeling Strategy 
**Baseline**: 

-
-
-

Machine learning model
Lightgbm
Ensemble 
Distillation
teacher/student

**Features**:

-
-
-
-
-

**Target Variable**: 

---
## 🚀 Running Instructions 

### 1. Clone the repository
Open a terminal and run: 
```
git clone https://github.com/Austinsucy/F3-Frost-Data-Challenge---Data-Slayers/
```

### 2. Install dependencies
```
pip install -r requirements.txt
```
### 3. Start Jupyter
Run either: 
```
jupyter notebook 
```
or 
```
jupyter lab
```
### 4. Open and run `final_notebook.ipynb`
- Run all cells in order
- Outputs include 

For comparison to traditional heuristics, open and run `baseline.ipynb` 

---

## 📄 Project Report
For a full overview of our methodology, modeling strategy, plots, diagrams, and discussion, see `DataSlayers_report.pdf` 📘

---

## ⚔️ Team Data Slayers
- Austin Tathong
- Donovan Butler
