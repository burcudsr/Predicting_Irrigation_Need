# 💧 Predicting Irrigation Need

This Machine Learning project aims to predict irrigation needs (Low, Medium, High) based on soil properties, environmental conditions, and crop growth stages. This study was developed as part of the **Kaggle Playground Series - Season 6, Episode 4**.

### 🚀 Live Demo
Test the model here: [Irrigation Need Prediction App](https://huggingface.co/spaces/bdaser/Irrigation)

### 📌 Problem Definition
The primary goal is to classify irrigation requirements by analyzing parameters such as soil moisture, pH levels, climatic data, and crop growth stages.

### 📊 Dataset
* **Training Data**: 630,000 entries.
* **Test Data**: 270,000 entries.
* The dataset is complete, with no missing values reported in the features.

### 🛠️ Feature Engineering
To improve the predictive power of the models, new features were derived to capture interactions between environmental factors:
* **Ratios and Indices**: Created features such as `ec_moisture_ratio`, `ph_carbon_interaction`, and `dryness_index` to reflect soil-water dynamics.
* **Micro-climate Effects**: Derived variables like `evapotranspiration_risk`, `sunlight_thermal_load`, and `mulch_temp_exposure` to simulate the impact of environmental conditions and mulching on topsoil.
* **Encoding**: Low-cardinality columns were processed using `get_dummies`, while structural features were processed using `OrdinalEncoder`.

### 🏆 Model Performance
The modeling results indicate that the **RandomForestClassifier** achieved the highest performance.

| Model | Accuracy | Precision | Recall | F1 Score |
| :--- | :--- | :--- | :--- | :--- |
| **RandomForestClassifier** | **0.9832** | **0.9832** | **0.9832** | **0.9832** |
| GradientBoostingClassifier | 0.9616 | 0.9616 | 0.9616 | 0.9616 |
| DecisionTreeClassifier | 0.9475 | 0.9475 | 0.9475 | 0.9475 |
