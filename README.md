# F1 Driver Performance Analysis Using Lap Times, PCA & Ensemble Models

This project explores what factors influence Formula 1 driver performance by analyzing lap time data and race metadata from the 2023 season. The goal is to model lap time as a key metric and uncover hidden performance patterns using statistical analysis, clustering, and machine learning.

## 📌 Project Goal
To predict and interpret Formula 1 driver lap times based on multiple race conditions and driver-related features — eventually building an interactive dashboard to simulate performance outcomes.

---

## 🛠️ Tools & Technologies
- Python
- pandas, numpy
- scikit-learn (RandomForest, PCA, KMeans)
- seaborn, matplotlib
- SHAP (planned)
- XGBoost (planned)
- Streamlit (planned)

---

## 🔄 Workflow

### 1. Data Loading & Preprocessing
- Combined multiple Kaggle-provided CSVs from the 2023 season
- Normalized time features (e.g., `sessionTime`, `lapTime`) to seconds for analysis
- Cleaned and merged data to align drivers, events, and laps

### 2. Exploratory Analysis
- Plotted lap times vs. lap number for each driver at each event
- Highlighted fastest lap for every driver visually
- Identified fastest and slowest laps across the dataset

### 3. Outlier Detection
- Created boxplots of fastest lap times per driver to spot outliers
- Found a consistent cluster of extreme values on the right (not random)
- Applied PCA to explore feature patterns that may explain these outliers

### 4. Clustering
- Used PCA-reduced features to cluster outlier vs. non-outlier drivers
- Identified subgroups based on lap time characteristics

### 5. Modeling
- Selected lap time as the target variable
- Built a Random Forest regressor to predict lap times
- Used k-fold cross-validation to avoid data snooping
- Extracted preliminary feature importances to guide SHAP analysis

### 6. Weather Data Integration
- Preprocessed track temperature and weather metadata
- Visualized weather–lap time relationships (planned for deeper analysis)

### 7. Next Steps (Planned)
- Add SHAP values to interpret model output
- Test XGBoost and compare with Random Forest
- Build a Streamlit dashboard for driver-based scenario simulation

---

## 📸 Sample Visuals (To Include Later)
- Driver lap time line plots (with fastest lap marked)
- Boxplots of fastest laps with outlier clusters
- PCA scatter plot of outliers vs. others
- Random Forest feature importance bar chart

---

## 🔗 Dataset
- [Formula 1 2023 Data (Kaggle)](https://www.kaggle.com/datasets)

---

## 🚧 Status
🟡 In Progress  
EDA, PCA, clustering, and Random Forest modeling completed. SHAP analysis and dashboard development planned.

---

## 📂 Repository Structure
├── data/ # Raw F1 datasets (excluded from repo)
├── f1_driver_analysis.ipynb # Main notebook
├── images/ # Diagnostic plots and model visuals
├── README.md # Project overview

## 👤 Author
**Heman** — Data Science undergrad focused on applying ML to real-world performance and behavioral data.
