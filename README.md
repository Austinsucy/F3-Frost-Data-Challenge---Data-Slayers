# ❄️ Data Slayers - Frost Risk Forecast Data Challenge

This repository contains our team's work for the **F3 frost risk forecast data challenge**, hosted by **UC San Diego** and the **National Data Platform (NDP)**. 

Our goal was to develop a machine learning model to accurately predict **frost risk 3, 6, 12, 24 hours ahead** using meteorological, environmental, and temporal features, and compare these predictions to baseline heuristics. 

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

Provided by the **California Irrigation Management Information System**, this dataset includes **hourly meteorological measurements from 2010-2025** across **18 weather stations** within California. 

**Data files:**    
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

Each file contains:
- Air temperature
- Relative humidity
- Dew point
- Soil temperature
- Solar radiation
- Wind speed & direction
- Reference evapotranspirtation (ETo)
- Hourly timestamps + QC flags

---

## 💭 Modeling Pipeline 
### Features:     
- Meteorological features
  - Temperature, humidity, dew point, wind, radiation, soil temp
- Derived physical variables
  - Dewpoint depression
  - Cooling rate
  - Humidity and wind interactions
- Time-based features
  - Lagged air temperatures
  - Rolling statistics
  - Cos/sin hour of day, day of year encodings
- Station metadata
  - Station IDs

### Target Variable:  
A binary frost risk indicator, defined as:   
- `1` if temperature `T ≤ 0°C` within the next `3`, `6`, `12`, or `24` hours 
- `0` otherwise (no frost event)

## 🤖 ML Models:   
We implemented a general model using `LightGBM Gradient Boosting` and a more innovative model using `Stacked Ensemble Knowledge Distillation`, which:

- Combines tree-based models
- High-capacity "teacher" models train a simpler "student" model
- Student preserves performance while reducing inference cost

**Baseline Heuristics**  
In order to compare the effectiveness of our machine learning models, we implemented traditional frost-forecasting rules widely used in agriculture, including:

- Climatology baseline
- Dew point empirical rule
- Persistence heuristics

---

## 🚀 Running Instructions 

### 1. Clone the repository
Open a terminal and run: 
```
git clone https://github.com/Austinsucy/F3-Frost-Data-Challenge---Data-Slayers/
cd F3-Frost-Data-Challenge---Data-Slayers
```

### 2. Install dependencies
```
pip install -r requirements.txt
```

### 3. Start Jupyter
Run either:   
`jupyter notebook`  
or   
`jupyter lab`

### 4. Open and run `f3_data_challenge_main.ipynb`
- Run all cells in order 

This notebook includes:
- Data loading & preprocessing
- Feature engineering
- Model training
- Evaluation (AUC, precision/recall, confusion matrices)
- Frot-risk forecast visualizations

For comparison to traditional heuristics, open and run `baseline.ipynb` 

---

## 📄 Project Report
For a detailed write-up of our methodology, modeling strategy, visualizations, and discussion, see:    

👉 `DataSlayers_report.pdf` 

---

## 👥 Team Data Slayers
- **Austin Tathong**
- **Donovan Butler**
