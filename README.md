# 🏠 Airbnb Listings Data Analysis Project: Pricing and Demand in the Short-Term Rental Market

## 🎯 Project Overview

This project presents an **end-to-end Exploratory Data Analysis (EDA)** of Airbnb listings data, focusing on the highly dynamic **Hospitality and Short-term Rentals** domain. The analysis addresses the challenge faced by hosts and investors in **determining optimal pricing strategies and identifying high-value properties** in a competitive market. It demonstrates comprehensive data processing, sophisticated visualization techniques (including geospatial mapping), and the derivation of actionable business insights.

### Project Objectives

1.  **Data Preparation Mastery:** Demonstrate robust data cleaning and type correction (e.g., converting price strings to numeric).
2.  **Comprehensive Exploratory Data Analysis (EDA):** Conduct univariate, bivariate, and multivariate analysis to uncover pricing and demand patterns.
3.  **Visualization and Insight Generation:** Generate **meaningful visualizations** (using Seaborn and Matplotlib) to support **key business insights and recommendations**.
4.  **Documentation and Presentation:** Maintain a well-structured and well-commented Jupyter Notebook for clear methodology and result interpretation.

---

## 💾 Data Source and Requirements

* **Dataset:** Airbnb Open Data (Source: Kaggle).
* **Domain:** Hospitality / Short-term Rentals.
* **Size:** Over 500 rows and 10 features (columns).

### Key Columns Analyzed:

| Column Name | Description | Role in Analysis |
| :--- | :--- | :--- |
| `price` | Nightly price of the listing. | **Target Variable** for distribution and correlation. |
| `room_type` | Type of accommodation (e.g., Entire home/apt). | Key categorical variable for market segmentation. |
| `neighbourhood`, `lat`, `long` | Geographical location data. | Essential for **Geospatial and Locational Pricing** analysis. |
| `minimum_nights` | Host-imposed operational constraint. | Used for host strategy and operational efficiency analysis. |
| `reviews_per_month` | Proxy for demand and booking activity. | Used to detect seasonality and popularity. |

---

## ⚙️ Methodology and Analysis Highlights

### 1. Data Cleaning and Pre-processing Summary

The data was prepared for analysis through a series of robust cleaning and transformation steps:

* **Duplicate Handling:** All duplicate rows were identified and removed.
* **Column Standardization:** Columns were renamed to a single, standard naming convention for consistency.
* **Feature Reduction (Dropping Columns):** Irrelevant or redundant columns (`id`, `host_id`, `license`, and `house_rules`) were dropped.
* **Data Type Correction:** The `price` and `service_fee` columns were converted from string to a **numeric (Float) type**.
* **Missing Value Imputation:** Null values in `reviews_per_month` were imputed with `0`, and those in `last_review` were set to a standard date (`01/01/1900`) to enable datetime operations.

### 2. Key Visualizations & Techniques

| Visualization Type | Insight Derived | Python Tool |
| :--- | :--- | :--- |
| **Geospatial Scatter Plot** | Identified clusters of high-priced listings, confirming **location as the primary price driver**. | GeoPandas, Contextily |
| **Bar Plot** | Showed that **'Entire home/apt' listings require higher average minimum nights** across all geographic groups. | Seaborn (`barplot`) |
| **Box Plots** | Compared the central tendency and spread of price distributions across room types. | Seaborn (`boxplot`) |
| **Correlation Heatmap** | Determined statistical relationships between numerical features (`price`, `number_of_reviews`, etc.). | Seaborn (`heatmap`) |

---

## 💡 Key Business Insights

1.  **Location Premium is Non-Negotiable:** The geospatial analysis confirms that **geographical location is the single most critical factor** influencing a listing's price, with strong clustering of high-value properties in central areas.
2.  **Strategic Minimum Nights:** 'Entire home/apt' listings enforce a significantly **higher average minimum night requirement**. This suggests hosts are optimizing these higher-value properties for **revenue stability and lower turnover costs** rather than maximizing short-term occupancy.
3.  **Market Composition:** **'Entire home/apt' listings make up the largest percentage** of the market supply, confirming the dominance of full property rentals.
4.  **Demand and Reputation:** High booking activity (proxied by reviews) correlates with higher pricing, indicating that **social proof and reputation justify a price premium** in the guest's perception.
5.  **Host Scale vs. Price:** A small percentage of large-scale hosts dominate inventory, but their pricing strategy is often competitive (aiming for high occupancy) rather than maximizing top-tier prices.

---

## 🚀 Conclusion and Recommendations

The project successfully analyzed the Airbnb dataset, revealing that **Location, Room Type, and Host Strategy** are the primary determinants of market success.

### Actionable Recommendations:

* **Optimize Operational Constraints:** Hosts of 'Entire home/apt' properties should set the minimum night requirement higher than the average for private rooms to reduce turnover costs and stabilize revenue.
* **Price Strategically:** Use the geospatial analysis to set a premium base price relative to the specific neighborhood, rather than relying on a flat seasonal model.
* **Prioritize Reviews:** Focus on maximizing a positive guest experience to build a strong review score, which serves as justification for premium pricing and boosts listing visibility.

---

## 🛠️ Technology Stack

* **Programming Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Geospatial Analysis:** **GeoPandas, Shapely, Contextily**

---

## 📬 Contact

**SWETHA E V**  
📧 swethaev14@hmail.com  
🔗 [LinkedIn](https://in.linkedin.com/in/swethaev)

---
