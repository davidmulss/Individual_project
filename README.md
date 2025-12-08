# Decoding the Boston Airbnb Market
### Leveraging Data Science to Optimize Pricing Strategies

**Author:** David Mulas Zelenskaya  
**Course:** DATA 6150 - Data Science Foundations  
**Term:** Fall 2025  
**Institution:** Wentworth Institute of Technology

---

## 📌 Project Overview
This project investigates the determinants of Airbnb rental prices in Boston to understand the market dynamics of the modern sharing economy. Using a dataset from September 2025, the study aims to identify key pricing drivers—such as location, room type, and host reputation—and predicts listing prices using quantitative modeling.

The analysis compares two regression models to determine which best captures the valuation of short-term rentals:
1.  **Multiple Linear Regression (MLR):** For baseline interpretability.
2.  **Random Forest Regression:** For capturing non-linear relationships and neighborhood "hotspots."

## 📂 Repository Structure
This repository is organized into four main folders as per the project requirements:

* **`report/`**: Contains the final written report in both Word (`.docx`) and PDF formats.
* **`codes/`**: Contains the Jupyter Notebook (`.ipynb`) with all data cleaning, EDA, and modeling scripts.
* **`data/`**: Contains the raw dataset used for analysis (`listings.csv.gz`).
* **`graph/`**: Contains the generated visualizations (histograms, boxplots, correlation matrices, and feature importance charts).

## 📊 Dataset
* **Source:** [Inside Airbnb](http://insideairbnb.com/get-the-data)
* **File:** `listings.csv.gz` (Boston, MA)
* **Snapshot Date:** September 23, 2025
* **Description:** The dataset contains approximately 4,000 listings and 75 distinct variables, including price, neighborhood, room type, and review scores.

## 🛠️ Methodology & Tools
**Language:** Python 3.x  
**Libraries Used:**
* `pandas` & `numpy` (Data Manipulation)
* `matplotlib` & `seaborn` (Visualization)
* `scikit-learn` (Machine Learning: Linear Regression, Random Forest, Metrics)

**Key Steps:**
1.  **Data Cleaning:** Removed price outliers (>$1,500), handled missing values, and encoded categorical variables (One-Hot Encoding).
2.  **EDA:** Visualized price distributions and correlations.
3.  **Modeling:** Trained models on an 80/20 train-test split.
4.  **Evaluation:** Compared models using RMSE and R-squared metrics.

## ❓ Research Questions & Answers
This project addressed three specific analytical questions:

**1. What are the main factors that influence Airbnb rental prices?**
* **Answer:** Feature importance analysis identified **Location (Neighbourhood)** and **Room Type** as the dominant drivers. Operational metrics like `number_of_reviews` play a secondary role.

**2. How do location-based features affect average rental prices?**
* **Answer:** Location acts as a non-linear price multiplier. Specific "hotspots" (neighborhoods) interact with property characteristics to create valuation tiers that simple linear models cannot capture effectively.

**3. Can we predict the price of a listing based on property characteristics?**
* **Answer:** Yes, but with limitations. The **Random Forest** model achieved an **R² of 0.43**, significantly outperforming Linear Regression. However, roughly 50% of price variance remains unexplained, likely due to qualitative factors (photos, decor) not present in the tabular data.

## 📈 Key Results
The **Random Forest Regression** model proved to be the superior method for predicting Airbnb prices in Boston.

| Model | RMSE (Error) | R-squared (Accuracy) |
| :--- | :--- | :--- |
| **Multiple Linear Regression** | $139.54 | 0.3107 |
| **Random Forest Regression** | **$126.77** | **0.4310** |

## 🚀 How to Run
1.  Clone this repository.
2.  Ensure you have the required libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Navigate to the `codes/` folder and launch the Jupyter Notebook.
4.  Run all cells to reproduce the analysis and generate the graphs.

---
*This project was completed as the Final Individual Project for DATA 6150.*
