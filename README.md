# Airbnb-price-prediction-bengaluru
ML model to predict Bengaluru Airbnb prices using XGBoost

# 🏡 Bengaluru Airbnb Price Prediction

This project uses real Airbnb listing data from Bengaluru to build a machine learning model that predicts listing prices. The goal is to extract value from textual features, amenities, and geolocation data to create a robust price estimation engine using XGBoost.

## 📊 Dataset Overview
- Source: Kaggle-style scraped dataset of listings in Bengaluru
- Size: ~20,000 entries
- Features: Textual description, amenities, review scores, location (lat/lon)

## 🧠 Features Extracted
- Average availability
- Amenity count
- Listing title/description length
- Presence of keywords (`wifi`, `luxury`, `budget`, etc.)
- Geolocation clusters via KMeans
- Sentiment polarity (via TextBlob)

## 🔧 Model Details
- Algorithm: XGBoost Regressor
- Tuned via: `GridSearchCV` on 3 parameters
- Best Parameters: `{ 'learning_rate': 0.01, 'max_depth': 5, 'n_estimators': 200 }`

## 📈 Final Performance
- RMSE: ₹109.98  
- R² Score: 0.37 (on test data)

## 📌 Future Enhancements
- Add NLP pipeline (e.g., TF-IDF + linear model)
- Deploy with Streamlit as an interactive pricing app
- Incorporate image features from listing thumbnails

---

_⭐ Created by Abinandanan R using Python, Pandas, XGBoost & scikit-learn_
