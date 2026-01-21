# Hazardous Asteroid classification

This project uses machine learning to classify whether asteroids are hazardous based on various orbital and physical parameters provided by NASA's NeoWS (Near Earth Object Web Service).

### Overview
The goal of this project is to build a predictive model that identifies potentially hazardous asteroids (PHAs). By analyzing features such as absolute magnitude, estimated diameter, and relative velocity, the model learns to distinguish between safe and dangerous celestial objects.

### Dataset
The project utilizes the NASA Asteroids Classification dataset from Kaggle.

Shape: 4,687 entries and 40 columns.

Target Feature: Hazardous (Boolean).

Key Features:

Absolute Magnitude.

Estimated Diameter (min/max in KM, M, Miles, Feet).

Relative Velocity (km/sec, km/hr, mph).

Orbit parameters (Eccentricity, Inclination, Orbital Period, etc.).

### Data Exploration and Cleaning
Initial Inspection: The dataset begins with 4,687 entries and 40 columns.

Feature Removal: Several columns deemed unnecessary for classification were dropped, including identifiers like Neo Reference ID, Name, and Orbit ID, as well as date-related fields like Close Approach Date and Orbit Determination Date.

Redundancy Handling: Non-numeric or redundant columns such as Orbiting Body (which only contained "Earth") and Equinox (which only contained "J2000") were removed to streamline the model.

### Data Visualization
Correlation Analysis: A heatmap was generated to identify relationships between features. This helped in understanding which orbital parameters and physical characteristics (like absolute magnitude and velocity) are most closely related.

Target Distribution: The notebook examines the distribution of the Hazardous label to understand class balance.

### Model Training and Evaluation
The notebook implements a supervised learning approach:

Data Splitting: The data was split into training and testing sets to evaluate performance on unseen data.

Algorithm Used: An XGBoost Classifier was employed for the final classification task.

Performance Metrics: The model's effectiveness was measured using:

Accuracy Score: To see the overall percentage of correct predictions.

Confusion Matrix: To visualize true positives vs. false positives.

Classification Report: Providing precision, recall, and F1-score for both hazardous and non-hazardous classes.


### Result:
Obtained an accuracy of 99.64%
