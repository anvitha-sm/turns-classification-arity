# Turn Classification – Arity 1A

## Overview
This project classifies vehicle maneuvers—like turns, lane changes, and U-turns—using telematics and sensor data. The insights can help improve driver safety, usage-based insurance, and autonomous vehicle systems.

## Approach
- **Data Preparation:** Cleaned and standardized GPS & MEMS sensor data, augmented features (speed, acceleration, turn intensity, etc.), handled outliers.  
- **Modeling:** Explored clustering models (HDBSCAN, K-Means, GMM) to identify driving patterns.  
- **Evaluation:** Used Silhouette, Davies-Bouldin, and Calinski-Harabasz metrics; visualized clusters with Folium maps.  
- **Final Pipeline:** Split data by left/right turns, ran HDBSCAN, and manually labeled clusters by risk (high, medium, low).

## Key Features
- Acceleration, speed, radius, angle change  
- Turn intensity & normalized turn intensity  
- Time of day, rush hour, path straightness  

## Tools
- **Data Handling:** Pandas, NumPy, GeoPandas  
- **Machine Learning:** Scikit-Learn  
- **Visualization:** Folium, Seaborn  

## Team
- Neha Hingorani – UCSC  
- Abhinaya Guduru – UT San Antonio  
- Hector Rios – San Jose State University  
- Anvitha Mattapalli – UCLA  
- Arya Yadav – Arizona State University  
- Sreenidhi Challagundla – UC Irvine  

## Next Steps
- Further analyze aggressive/unusual clusters  
- Build a supervised classification model
