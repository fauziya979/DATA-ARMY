# DATA-ARMY

📊 Project Overview
This project offers a comprehensive analysis of global agricultural productivity from 1990 to 2013, leveraging machine learning techniques to predict crop yields and identify key drivers. The analysis covers 101 countries and 10 crop types, providing insights for farmers, policymakers, and agricultural researchers facing challenges from climate change.

Key Objectives
•	Analyze historical crop yield data and associated environmental/climate features

•	Apply machine learning models to predict future crop yields

•	Identify key factors that significantly influence agricultural productivity

•	Provide actionable insights for optimizing agricultural practices

📋 Dataset

•	Period: 1990-2013

•   Records before Cleaning : 28,242

•	Records: 25,932 (after cleaning)

•	Countries: 101 (India most frequent)

•	Crops: 10 (Potatoes most frequent)

Dataset Features

•	Target variable: hg/ha_yield (hectogram per hectare)

Key Predictors

•	avg_temp (average temperature in °C)

•	average_rain_fall_mm_per_year

•	Area (country)

•	Item (crop type)

•	Year

•	pesticides_tonnes


🔧 Methodology

Data Preprocessing

•	No missing values were recorded

•	Removed duplicates (2,310 rows)

•	Handled outliers using IQR method

•	Applied feature engineering (polynomial features, binary features)

•	Applied categorical encoding (one-hot encoding)

•	Standardized numerical features

Exploratory Data Analysis

•	Temporal trend analysis (1990-2013)

•	Correlation analysis of numerical features

•	Environmental factor analysis (rainfall, temperature)

•	Resource impact analysis (pesticide usage)

•	Crop-specific analysis

Machine Learning Models

•	Linear Regression

•	Lasso Regression

•	Ridge Regression

•	Decision Tree Regressor

•	K-Nearest Neighbors (KNN) Regressor

🔍 Key Findings

Temporal Trends

•	27.2% increase in crop yields from 1990 to 2013

•	Year is a significant predictor (correlation: 0.243)

Pesticide Impact

•	High pesticide usage increased yields by 25.1%

•	Strongest predictor with crop-specific variations

Environmental Factors

•	Rainfall: Weak correlation (0.013), with 4.2% higher yields above 2,000 mm/year

•	Temperature: 21.0% higher yields above 30°C, challenging heat stress assumptions

Model Performance

•	Decision Tree Regressor: R² = 0.9816, MAE = 3,294.61 hg/ha

•	KNN Regressor: R² = 0.9880, MAE = 3,548.45 hg/ha

•	Linear Models: R² ≈ 0.8014, MAE ≈ 22,780 hg/ha

📈 Visualizations

The project includes various visualizations:

•	Average crop yield over time

•	Correlation matrix of numerical features

•	Pesticide usage vs. crop yield

•	Mean yield by crop type and pesticide usage

•	Average rainfall vs. crop yield

•	Average temperature vs. crop yield

•	Average yield by temperature range

•	Distribution of crop types

•	Actual vs. predicted yields

💡 Recommendations

Model Improvements

•	Tune Decision Tree hyperparameters

•	Explore ensemble methods

•	Add more polynomial features for environmental factors
Data Expansion

•	Incorporate post-2013 data

•	Add features like soil type, irrigation, or crop genetics

•	Balance crop and country representation

Policy Implications

•	Optimize pesticide use based on crop-specific benefits

•	Promote heat-tolerant crops in high-temperature regions

•	Support agricultural innovation to sustain yield increases

🚀 Getting Started

Prerequisites

pandas

numpy

matplotlib

seaborn

scipy

scikit-learn

Installation

bash

git clone https://github.com/yourusername/crop-yield-analysis.git
cd crop-yield-analysis

pip install -r requirements.txt

Usage

python

# Load the trained model

import pickle

with open('models/dtr.pkl', 'rb') as f:

    model = pickle.load(f)

# Load the preprocessor

with open('models/preprocessor.pkl', 'rb') as f:

    preprocessor = pickle.load(f)

# Make predictions

X_transformed = preprocessor.transform(X_new)

predictions = model.predict(X_transformed)

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

🙏 Acknowledgments
•	Thanks to all contributors who have invested their time in improving this project
•	Special thanks to the agricultural research community for providing valuable datasets

