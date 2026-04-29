# msbd570-final-project-evannbailey
Interactive visual analytics dashboard for identifying autonomic signatures of stroke risk in OSA patients using SHHS data. Final project for MSBD 570.

# High-Dimensional Autonomic Profiling: Stroke Risk Visualization Framework
**Course:** MSBD 570: Data Visualization - Final Project  
**Author:** Evann Bailey  
**Department:** Biomedical Data Science, Meharry Medical College  
**Version:** v1.0 (Final Submission)

---

## 1. Summary
This project introduces an interactive visual analytics dashboard designed to address the diagnostic gap in stroke risk prediction for patients with Obstructive Sleep Apnea (OSA). 

While the current clinical standard—the Apnea-Hypopnea Index (AHI)—often fails to provide statistically significant hazard ratios for individual stroke events, this framework visualizes a unique **"Autonomic Phenotype."** By analyzing high-resolution ECG signal transitions from the Sleep Heart Health Study (SHHS), the tool identifies physiological instability and "pathological divergence" that remains hidden in aggregate clinical counts.

## 2. Key Visual Analytics & Insights
* **Parallel Coordinates Plot:** Visualizes the "Fanning Effect" across 20 high-dimensional features. It specifically isolates the variance in Hjorth Complexity during the "Exit-Transition" window (re-entry from apnea to normal breathing).
* **PCA Spatial Clustering:** Reduces 20 clinical and signal dimensions into a 2D map to reveal a distinct **"Stroke Drift"**—a spatial separation where high-risk cases migrate away from the homeostatic control cluster.
* **Correlation Heatmap:** Validates the independence of Deep-Learned (CNN) morphological features from traditional heart rate variability (HRV) metrics, proving that computer vision captures latent physiological "glitches."
* **Interactive Brushing:** Enables real-time risk stratification by allowing users to filter high-complexity axes to isolate 80%+ of the stroke cohort.

## 3. Technical Infrastructure
* **Language:** Python 3.9+
* **Dashboard Framework:** Plotly Dash
* **Data Processing:** Pandas, NumPy, Scikit-Learn
* **Version Control:** GitHub v1.0 Tagged Release
* **Pre-processing:** All features are Z-score normalized to ensure visual parity across disparate clinical scales.

## 4. Setup and Installation

### Step 1: Clone the Repository
```bash
git clone [https://github.com/Evann-Bailey/msbd570-final-project-evannbailey.git](https://github.com/Evann-Bailey/msbd570-final-project-evannbailey.git)
cd msbd570-final-project-evannbailey

### Step 2: Run
python app.py

## 5. Clinical Context
Data is sourced from the Sleep Heart Health Study (SHHS). Features were extracted using a Linux HPC cluster at Meharry Medical College.

