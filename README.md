# Arity Turn-Classification AI Studio Project

---

### 👥 **Team Members**

| Name                   | GitHub Handle | Contribution                                                |
| ---------------------- | ------------- | ----------------------------------------------------------- |
| Abhinaya Guduru        | @abhinaya-03  | Data exploration, preprocessing, clustering experimentation |
| Hector Rios            | @Hrios05      | Feature engineering, clustering pipelines, model evaluation |
| Anvitha Mattapalli     | @anvitha-sm   | Data cleaning, EDA, feature alignment                       |
| Neha Hingorani         | @antsfly626   | Model comparison, validation metrics, visualization         |
| Sreenidhi Challagundla | @sreenidhi608 | Cluster labeling, business insights, Folium mapping         |

---

## 🎯 **Project Highlights**

* Developed an unsupervised learning pipeline to cluster and classify driving maneuvers using vehicle telematics and sensor data.
* Applied HDBSCAN, K-Means, and GMM across multiple data subsets (iOS, Android, combined) to identify meaningful driving behavior patterns.
* Achieved a best Silhouette Score of ~0.59 using HDBSCAN for high-dimensional maneuver data.
* Generated actionable insights to support driver safety programs, insurance risk pricing, and autonomous vehicle research at Arity.

---

## 👩🏽‍💻 **Setup and Installation**

1. Clone the repository:

   ```bash
   git clone <repo-url>
   cd <repo-name>
   ```
2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Ensure access to the telematics dataset (provided through AI Studio / Arity).
5. Run the notebooks or scripts in order:

   * Data preprocessing & feature engineering
   * Clustering experiments
   * Evaluation & visualization

---

## 🏗️ **Project Overview**

This project was completed as part of the **Break Through Tech AI Program – AI Studio**, in partnership with **Arity**. The goal was to analyze vehicle telematics and sensor data to classify driving maneuvers such as left turns, right turns, U-turns, and straight driving.

Understanding these patterns enables improved driver safety insights, supports usage-based insurance pricing, and contributes to autonomous vehicle system development.

---

## 📊 **Data Exploration**

* **Data Source:** Vehicle telematics and MEMS/GPS sensor data
* **Data Type:** Time-series sensor measurements and derived driving features
* **Preprocessing Steps:**

  * Removed nonsensical and internal-only features
  * Handled missing values and outliers using winsorization
  * Aligned features across GPS and MEMS sensors
  * One-hot encoded categorical features
  * Applied safe standardization excluding geographic and temporal fields

EDA revealed strong relationships between acceleration, angular change, speed, radius, and turn intensity.

---

## 🧠 **Model Development**

* **Models Tested:**

  * HDBSCAN
  * K-Means
  * Gaussian Mixture Models (GMM)
* **Validation Metrics:**

  * Silhouette Score
  * Davies-Bouldin Index
  * Calinski-Harabasz Score
* **Approach:**

  * Split data by left and right turns
  * Ran clustering models on multiple subsets (iOS, Android, combined)
  * Used custom grid search for unsupervised hyperparameter tuning

HDBSCAN was selected as the final model due to its ability to handle high-dimensional data and discover arbitrarily shaped clusters.

---

## 📈 **Results & Key Findings**

* Successfully identified clusters corresponding to distinct driving behaviors
* Labeled clusters into risk categories:

  * **High Risk:** Extreme and sharp turns
  * **Medium Risk:** Moderate and mixed minor turns
  * **Low Risk:** Gentle and straight-like turns
* Feature importance analysis highlighted acceleration, distance, angle change, speed, radius, and turn intensity as key drivers

Folium visualizations confirmed spatial consistency of cluster labels.

---

## 🚀 **Next Steps**

* Further investigate edge-case and failure clusters
* Transition from unsupervised clustering to supervised classification
* Build a real-time dashboard to visualize driver behavior insights

---

## 📝 **License**

This project is licensed under the MIT License.

---

## 🙏 **Acknowledgements**

Thank you to our AI Studio Coach, Challenge Advisor, and the Break Through Tech team for guidance and support throughout the project.
