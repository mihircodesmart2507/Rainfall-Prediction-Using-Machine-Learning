# Rainfall-Prediction-Using-Machine-Learning
An end-to-end project analyzing historical weather data, performing EDA, feature selection, model training, and visualizations to predict rainfall accurately, with insights and performance evaluation charts included


## 📌 Project Overview

This project focuses on predicting rainfall using machine learning techniques by analyzing historical weather data. Accurate rainfall prediction plays a crucial role in agriculture, water resource management, disaster preparedness, and climate analysis.

The project follows a complete machine learning pipeline including data preprocessing, exploratory data analysis (EDA), feature engineering, model training, evaluation, and visualization.

---

## 🎯 Objectives

* Analyze historical rainfall and weather data
* Identify key factors influencing rainfall
* Build and evaluate machine learning models for rainfall prediction
* Compare model performance using evaluation metrics
* Visualize trends, correlations, and predictions through charts and graphs

---

## 🧠 Machine Learning Workflow

1. **Data Collection & Processing**

   * Loaded and cleaned the dataset
   * Handled missing values and inconsistencies
   * Performed feature selection and transformation

2. **Exploratory Data Analysis (EDA)**

   * Distribution analysis of rainfall data
   * Correlation heatmaps to identify important features
   * Trend analysis using visual plots
   * Outlier detection

3. **Data Visualization**

   * Bar charts, line plots, and histograms
   * Correlation heatmaps
   * Model prediction vs actual rainfall plots
     *(All graphs and charts are available in the notebook)*

4. **Model Building**

   * Trained machine learning models for rainfall prediction
   * Split data into training and testing sets
   * Applied appropriate preprocessing techniques

5. **Model Evaluation**

   * Compared model performance using evaluation metrics
   * Analyzed accuracy and error rates
   * Visualized prediction results

---    


📊 Exploratory Data Analysis (EDA) & Visualizations   (You can see all the graphs in that file)

Before building the machine learning model, an in-depth Exploratory Data Analysis (EDA) was performed to understand the data distribution, relationships between variables, and potential patterns influencing rainfall.      


🔹 Feature Distribution Analysis
Histograms with KDE (Kernel Density Estimation) were plotted for all numerical weather parameters:


Pressure
Maximum Temperature (maxtemp)
Average Temperature
Minimum Temperature (mintemp)
Dew Point
Humidity
Cloud Cover
Sunshine
Wind Speed


* Key Observations:


Temperature-related features (maxtemp, temperature, mintemp) show near-normal distributions, indicating stable seasonal trends.
Humidity and cloud cover are skewed toward higher values, which is typical for rainy conditions.
Pressure shows slight variation, with lower pressure generally associated with rainfall.
Sunshine is negatively skewed, suggesting fewer sunshine hours on rainy days.
Wind speed has some extreme values, indicating occasional strong winds.       



# 🌧️ Rainfall Distribution
A count plot was used to analyze the target variable rainfall:


0 → No Rain, 1 → Rain


Insight:

The dataset is slightly imbalanced, with more rainy days than non-rainy days.
This imbalance is considered during model evaluation to avoid biased predictions.



# 🔥 Correlation Heatmap
A correlation heatmap was generated to understand relationships between features.
Important Correlations with Rainfall:


* Positive correlation:


Humidity
Cloud cover
Dew point


* Negative correlation:


Sunshine
Pressure
Temperature features show indirect influence through humidity and dew point.


Multicollinearity Notice:

Strong correlations exist between maxtemp, temperature, and mintemp.
Dew point is highly correlated with temperature and humidity.
This insight helps in feature selection and avoiding redundant inputs. 


# 📦 Boxplot Analysis (Outlier Detection)
Boxplots were created for all numerical features to identify outliers.
Findings:


Humidity, dew point, wind speed, and sunshine contain noticeable outliers.
Outliers represent extreme but realistic weather conditions (e.g., storms, heat waves).
These values were retained to preserve real-world weather behavior.



✅ Summary of EDA Insights


Rainfall is strongly influenced by humidity, cloud cover, and dew point.
Sunshine and pressure act as inverse indicators of rainfall.
Temperature features are highly correlated and should be handled carefully.
The dataset reflects realistic weather variability, making it suitable for ML modeling.
This EDA phase ensured better feature understanding and informed model selection for accurate rainfall prediction.





## 📊 Technologies & Tools Used

* **Programming Language:** Python
* **Libraries:**

  * NumPy
  * Pandas
  * Matplotlib
  * Seaborn
  * Scikit-learn
* **Environment:** Jupyter Notebook

---

## 📈 Results & Insights

* Identified key weather parameters influencing rainfall
* Visual analysis helped understand seasonal and trend-based patterns
* Machine learning models demonstrated reliable prediction performance
* Graphical comparison of actual vs predicted rainfall enhanced interpretability

---

## 🚀 How to Run the Project

1. Clone this repository

   ```bash
   git clone https://github.com/your-username/rainfall-prediction-ml.git
   ```
2. Navigate to the project directory

   ```bash
   cd rainfall-prediction-ml
   ```
3. Open the Jupyter Notebook

   ```bash
   jupyter notebook
   ```
4. Run all cells in `Rainfall_Prediction_using_Machine_Learning.ipynb`

---

## 📌 Future Improvements

* Use advanced models like XGBoost or Random Forest tuning
* Deploy the model using Flask or FastAPI
* Integrate real-time weather data APIs
* Perform hyperparameter optimization
* Extend the project to region-wise rainfall forecasting


