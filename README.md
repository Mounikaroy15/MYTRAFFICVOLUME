# traffic-prediction-project
# 🚦 TrafficTelligence - Trip Duration Forecasting

This project predicts **trip duration** for green taxi rides using machine learning and provides an interactive **Streamlit app** for real-time predictions. It includes modules for data preprocessing, model training and evaluation, algorithm logic, and a deployment-ready web app.

---

## 📁 Project Structure
```bash
MYTRAFFICVOLUME/
├── data/               # Raw dataset files
├── notebooks/          # Jupyter notebooks for EDA and experimentation
├── src/                # Source code files
│   ├── data_preprocessing.py
│   ├── model_training.py
│   ├── prediction.py
│   └── visualization.py
├── outputs/            # Generated reports and saved models
├── requirements.txt    # Project dependencies
├── README.md           # Project overview
└── main.py             # Main executable script

```
---

## 📌 Modules Overview

### 1. cleaned_green_tripdata_2025_03.csv
Preprocessed green trip dataset including:
- `trip_distance`
- `pickup_hour`
- `is_weekend`
- `is_rush_hour`
- `trip_duration` (target)

---

### 2. data_preprocessing
Handles:
- Loading raw data
- Feature engineering (rush hour/weekend flags)
- Cleaning and formatting

---

### 3. algorithm
Contains:
- Linear Regression implementation
- Model training on selected features

### 4. evaluation
Handles:
- Test set prediction
- Metrics like:
  - **Mean Squared Error (MSE)**
  - **R-squared (R²)**
- Visualization:
  - Trip Duration Distribution
  - Distance vs Duration Scatter
  - Duration by Hour Barplot
  - Weekend vs Weekday Boxplot

---

### 5. app.py
An interactive web app for:
- Uploading the dataset
- Viewing dataset preview
- Predicting trip duration based on:
  - Distance
  - Pickup hour
  - Rush hour/weekend flags
  - Vehicle type (Car, Bike, Bus, Truck)
- Displaying traffic level & estimated vehicle volume
- Visual insights

Run it using:
```bash
streamlit run app.py
