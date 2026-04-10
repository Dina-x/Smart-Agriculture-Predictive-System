# Smart Agriculture: Multi-Output Predictive System 🌿

## 📋 Project Overview
This project focuses on precision agriculture by building an intelligent system that predicts multiple agricultural needs and risks simultaneously. Using a Multi-output Random Forest Classifier, the system analyzes environmental data to help farmers make data-driven decisions regarding irrigation and plant health.

---

## 🚀 Key Features & Goals
The model is designed to predict three critical targets at once:
1. Irrigation Decision: Determines if the land needs watering based on soil moisture and temperature.
2. Water Efficiency: Categorizes how efficiently water is being used (Levels 0 to 2).
3. Plant Stress Index: Identifies if the plant is under stress due to environmental factors.

---

## 🛠 Technical Implementation
* Data Engineering: Created custom labeling logic to derive Water_Efficiency and Plant_Stress from raw sensor data (Temperature, Humidity, and MOI).
* Architecture: Implemented a MultiOutputClassifier wrapping a Random Forest model, allowing for a single model to output multiple classifications.
* Preprocessing: Used LabelEncoder for categorical data and handled data cleaning/deduplication to ensure model reliability.

---

## 📊 Results & Analysis
Based on the model execution:
* High Accuracy: The model achieved excellent results across all three targets (Irrigation, Efficiency, and Stress).
* Performance Metrics:
    * Confusion Matrix: Shows that the model is particularly strong at identifying when irrigation is *not* needed, effectively reducing water waste.
    * Classification Report: Shows high Precision and Recall, meaning the model rarely misses a "Plant Stress" event and maintains low false alarms.
      ### 📈 Performance Metrics
      | Target Variable | Accuracy | Precision | Recall |
      | :--- | :---: | :---: | :---: |
      | Irrigation | 99% | 0.99 | 0.99 |
      | Water Efficiency | 98% | 0.98 | 0.98 |
      | Plant Stress | 99% | 0.99 | 0.99 |
* Data Insights: Visualizations (**Boxplots**) indicated that Soil Moisture (MOI) and Temperature are the most influential factors in determining plant health.

---

## 💻 Tech Stack
* Language: Python 
* Libraries: Scikit-learn, Pandas, NumPy, Matplotlib, Seaborn.
* Algorithm: Multi-output Random Forest Classifier.

