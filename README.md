# 🏨 Hotel Booking Demand Analysis & Cancellation Prediction

This project analyzes hotel booking demand and predicts cancellations using **machine learning models**.  
The goal is to identify key factors influencing cancellations and provide **business recommendations** for improving occupancy planning and revenue management.

## Project Overview
- Dataset: [Hotel Booking Demand Dataset (Kaggle)](https://www.kaggle.com/jessemostipak/hotel-booking-demand)  
- Rows: **119,390** | Columns: **32**  
- Period: **Jan 2015 – Jul 2017**  
- Industry Context: The hotel industry faces challenges from high cancellation rates (~30%), seasonal demand, and diverse market segments.

## Problem Statement
Hotel bookings face **~30% cancellations**, which negatively impacts:
- Occupancy planning  
- Resource management  
- Marketing strategy

This project aims to **analyze cancellation patterns** and **build predictive models** to reduce business risk.

## Workflow
1. **Data Understanding** – Explore dataset structure & quality  
2. **Data Preprocessing** – Handle missing values, duplicates, and data type conversions  
3. **EDA & Visualization** – Identify booking patterns, seasonality, and customer behaviors  
4. **Feature Engineering & Balancing** – Encode categorical features, scale numerics, and apply **SMOTE** for imbalance  
5. **Model Development** – Logistic Regression, Random Forest, and XGBoost  
6. **Model Evaluation** – Use confusion matrix, precision, recall, and hyperparameter tuning  
7. **Conclusion & Recommendations**

## EDA Highlights
- **Monthly Booking Trend**: Increasing trend in 2015–2016, with peaks during summer & year-end holidays.  
- **Lead Time vs Cancellation**: Longer lead times significantly increase cancellation likelihood.  
- **Market Segment**: Online/Offline Travel Agents account for most cancellations.  
- **Geographic Patterns**: Portugal had the highest number of cancellations.

## Machine Learning Models
- **Tested Models**: Logistic Regression, Random Forest, XGBoost  
- **Best Model**: **XGBoost** with **87% recall** after hyperparameter tuning  
- **Why XGBoost?**  
  - Best balance between recall & precision  
  - Captures most cancelled bookings while minimizing false negatives  

## Key Insights
- Longer lead time = higher risk of cancellation  
- Customers from Online Travel Agents cancel more frequently  
- Portugal contributes the highest cancellation rate  
- More special requests & booking changes = higher chance of cancellation  

## Business Recommendations
- Implement **deposit/penalty policies** for long lead-time bookings  
- Negotiate stricter deposit requirements with Online Travel Agents  
- Adjust **pricing strategies by region** (e.g., Portugal)  
- Send **automated reminders** (email/WhatsApp) for guests with long lead times and no special requests  


## Project Structure

├── hotel_booking.py # Streamlit app
├── hotel_bookings.csv # Dataset
├── requirements.txt # Dependencies
├── scaler.pkl # Preprocessing scaler
├── encoder.pkl # Encoder for categorical features
├── xgb_model.pkl # Trained XGBoost model
└── README.md # Project documentation

##🌐 Live Demo

👉 [Streamlit App](https://hotelbookingprediction.streamlit.app/)


👩‍💻 Author
Oktavindy

📍 Data Science Bootcamp @ dibimbing.id

🔗 ooktavindy@gmail.com

## How to Run Locally
```bash
# Clone repository
git clone https://github.com/oktafchen/hotel_booking_prediction.git
cd hotel_booking_prediction

# Install dependencies
pip install -r requirements.txt

# Run Streamlit app
streamlit run hotel_booking.py






