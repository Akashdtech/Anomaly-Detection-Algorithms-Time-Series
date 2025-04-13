# NYC-Taxi-Traffic-Anomaly-Detection-Time-Series
This project demonstrates how to detect anomalies in time-series data using multiple machine learning techniques. The dataset used is `taxitraffic.csv`, which contains timestamped traffic volume information. The goal is to identify unusual patterns or outliers that may indicate anomalies in taxi traffic.

## 📊 Techniques Implemented

Three popular unsupervised anomaly detection algorithms are applied:

- **Isolation Forest**
- **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**
- **Local Outlier Factor (LOF)**

## 🔍 Workflow Overview

1. **Data Loading & Exploration**:
   - Reads the `taxitraffic.csv` file.
   - Inspects data structure, checks for missing values, and summarizes key statistics.

2. **Feature Engineering**:
   - Converts the timestamp column to datetime format.
   - Extracts temporal features: hour, day of the week, and month.

3. **Preprocessing**:
   - Selects relevant features: `value`, `hour`, `dayofweek`, `month`.
   - Applies standard scaling using `StandardScaler`.

4. **Anomaly Detection Methods**:
   - **Isolation Forest**: Trains a model to isolate anomalies and visualizes them on a time-series plot.
   - **DBSCAN**: Uses density-based clustering to find outliers as noise points.
   - **LOF**: Identifies local density deviations of data points with respect to their neighbors.

5. **Visualization**:
   - Anomalies detected by each method are plotted on the time axis to show when unusual traffic patterns occur.

## 📦 Dependencies

- pandas
- numpy
- matplotlib
- scikit-learn

Install with:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## 📁 Dataset

Make sure the `taxitraffic.csv` file is placed in the same directory as the script. The dataset must contain at least:
- `timestamp`: datetime of the traffic record
- `value`: a numeric representation of traffic volume

## 📈 Output

Each model outputs:
- Anomaly scores and prediction labels
- A time-series plot with anomalies marked in red

## 🚀 Use Case

This pipeline is ideal for monitoring real-time traffic data and identifying potential issues such as data spikes, drops, or sensor malfunctions.
