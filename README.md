<div align="center">

# ✈️ **Airline Passenger Demand Forecasting using Time Series Models**

</div>

---

## 🧩 **Project Overview**

This project focuses on forecasting **monthly airline passenger traffic** using historical data that exhibits clear **trend** and **seasonality** patterns.  
By leveraging statistical time series models, the goal is to predict future passenger volumes to assist in **capacity planning**, **resource allocation**, and **strategic decision-making** for airline operations.  

Three forecasting models are implemented and compared — **Holt-Winters Exponential Smoothing**, **ARIMA**, and **SARIMAX** — to determine which provides the most accurate and stable forecasts.

---

## 🎯 **Objectives**

- Analyze and visualize monthly airline passenger trends and seasonality  
- Build and tune Holt-Winters, ARIMA, and SARIMAX forecasting models  
- Compare model accuracy and evaluate forecasting performance  
- Predict future passenger demand and visualize forecast intervals  
- Interpret findings for actionable insights in airline planning  

---

## ⚙️ **Key Methods**

1. **Time Series Decomposition** – To separate trend, seasonality, and residual components  
2. **Stationarity Testing** – Using Augmented Dickey-Fuller (ADF) test  
3. **Model Fitting & Parameter Selection** – Grid search for ARIMA/SARIMAX hyperparameters  
4. **Forecast Evaluation** – Based on metrics such as RMSE, MAPE, and AIC  
5. **Visualization** – Forecast plots with confidence intervals to interpret results  

---

## 📊 **Visualizations**

---

### 🧭 **Monthly Passenger Trend**
![Monthly Airline Passengers](./Monthly%20Airline%20Passengers.png)
**Description:** Displays long-term passenger growth and clear seasonal spikes in air travel.

---

### 📉 **Rolling Statistics**
![Rolling Statistics](./Rolling%20Statistics.png)
**Description:** Shows the rolling mean and standard deviation to assess stationarity in the time series.

---

### 🔍 **Decompose the Time Series**
![Decompose the Time Series](./Decompose%20the%20Time%20Series.png)
**Description:** Breaks the time series into **trend**, **seasonal**, and **residual** components for deeper understanding.

---

### 📈 **Holt-Winters Forecast vs Actual**
![Holt-Winters Forecast vs Actual](./Holt-Winters%20Forecast%20vs%20Actual.png)
**Description:** Displays how the Holt-Winters model effectively captures both trend and seasonality in the data.

---

### ⚙️ **ARIMA Forecast vs Actual**
![ARIMA Forecast vs Actual](./ARIMA%20Forecast%20vs%20Actual.png)
**Description:** Highlights ARIMA’s performance — captures trend but struggles with seasonality.

---

### 🌦️ **SARIMAX Forecast vs Actual**
![SARIMAX Forecast vs Actual](./SARIMAX%20Forecast%20vs%20Actual.png)
**Description:** Shows SARIMAX model’s superior fit, accurately modeling both seasonal and trend components.

---

## 📈 **Model Insights and Comparison**

This section summarizes the performance evaluation of the three forecasting models — **Holt-Winters**, **ARIMA**, and **SARIMAX** — applied to the airline passengers dataset.

---

### ✳️ **1. Holt-Winters Exponential Smoothing Forecast**

#### **Key Insights**
- Successfully captured both **trend** and **seasonality** in the data.  
- Forecasted values closely matched the **true test data**, especially during **seasonal peaks**.  
- Slight **underestimation at troughs** but strong overall alignment.  
- Ideal for datasets with **multiplicative seasonality**.

#### **Model Performance**
- **MAE:** `10.30`  
- **RMSE:** `15.81`

> ✅ **Conclusion:**  
Holt-Winters achieved the **lowest error** and provided the most accurate forecast.  
It serves as the **best-performing baseline model** for this dataset.

---

### ⚙️ **2. ARIMA Forecast**

#### **Key Insights**
- Accurately modeled the **overall upward trend** but **failed to capture seasonality**.  
- Forecasted curve appeared **too smooth**, missing periodic peaks and dips.  
- Unsuitable for datasets with **strong seasonal patterns**.

#### **Model Performance**
- **MAE:** `41.83`  
- **RMSE:** `55.22`

> ⚠️ **Conclusion:**  
ARIMA is **ineffective for seasonal datasets**; forecasts lacked seasonal structure and had high error values.

---

### 🌦️ **3. SARIMAX Forecast**

#### **Key Insights**
- Captured both **trend** and **seasonality** accurately.  
- Forecasts aligned closely with the actual data across the entire test set.  
- More robust than ARIMA, allowing inclusion of **exogenous regressors**.  

#### **Model Performance**
- **MAE:** `13.99`  
- **RMSE:** `17.20`

> ✅ **Conclusion:**  
SARIMAX produced **reliable and stable forecasts**, effectively modeling seasonal patterns with slightly higher complexity.

---

## 📊 **4. Model Comparison Summary**

| Model              | MAE    | RMSE   | Key Strengths                                      | Limitations |
|--------------------|--------|--------|----------------------------------------------------|--------------|
| **ARIMA**          | 41.83  | 55.22  | Captures overall trend                             | Fails to model seasonality |
| **Holt-Winters**   | 10.30  | 15.81  | Best accuracy, captures trend & seasonality         | Slight underestimation at troughs |
| **SARIMAX**        | 13.99  | 17.20  | Handles trend, seasonality, and exogenous factors   | Slightly higher RMSE than Holt-Winters |

---

## 🏆 **5. Final Conclusion & Recommendations**

- **Best Model:** 🥇 **Holt-Winters Exponential Smoothing**  
  - Lowest RMSE (`15.81`), best alignment with actual values, interpretable, and simple to implement.  
- **Runner-Up:** 🥈 **SARIMAX**  
  - Nearly as accurate, highly flexible, and suitable for advanced forecasting with external features.  
- **Least Effective:** 🚫 **ARIMA**  
  - Poor at modeling seasonal data and resulted in the highest RMSE (`55.22`).

> **Final Takeaway:**  
For datasets with **strong trend and seasonality**,  
- Use **Holt-Winters** for simplicity and accuracy.  
- Choose **SARIMAX** for complex scenarios or inclusion of external variables.  
- Avoid **ARIMA** unless data is non-seasonal or stationarized.

---

## 💡 **Key Insights & Outcomes**

- The airline passenger data shows **clear seasonality** and **long-term growth trend**.  
- **SARIMAX and Holt-Winters** are both suitable for forecasting, with Holt-Winters slightly outperforming.  
- Time series forecasting enables better **demand planning and operational forecasting** in the airline industry.  
- The models provide a framework extendable to similar business forecasting problems.

---

## 🧠 **Technologies Used**

- **Python 3.x**  
- **Pandas**, **NumPy** – Data manipulation and numerical computations  
- **Matplotlib**, **Seaborn** – Visualization  
- **Statsmodels** – Time series modeling (ARIMA, SARIMAX, Holt-Winters)  
- **Scikit-learn** – Evaluation metrics  
- **Jupyter Notebook** – Interactive development environment  

---

## 🛠️ **Setup & Installation Instructions**

1. **Clone this repository:**
   ```bash
   git clone https://github.com/yourusername/Airline-Passenger-Forecasting.git
   cd Airline-Passenger-Forecasting
   ```
2. Create a virtual environment (Optional):
   ```
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   venv\Scripts\activate      # Windows
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Launch the Jupyter Notebook:
   ```
   jupyter notebook Airline_Passenger_Forecasting.ipynb
   
---

## **▶️ Usage Instructions**

- Load the dataset (**airline-passengers.csv** data).
- Run the notebook `Airline_Passenger_Forecasting.ipynb` sequentially to preprocess data, visualize, and fit models.
- Evaluate model performance using RMSE and MAE.
- Visualize forecast results and confidence intervals.
- Compare forecasts across ARIMA, Holt-Winters, and SARIMAX.

---

## 🔗 Connect with Me

Let’s connect on LinkedIn for project discussions or data-driven collaborations:

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/indu-r-3a3767170/)

---

## 🙌 Feedback & Support

If you found this project helpful, please ⭐ star the repository and share your thoughts. Suggestions and contributions are always welcome!  
