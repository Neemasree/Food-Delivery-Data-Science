# Food Delivery Data Science Analysis

## 📌 Project Overview

This project analyzes food delivery rider-trip data to identify the major factors responsible for late deliveries and understand delivery performance across different distances, traffic conditions, hours, and areas.

The analysis was completed in two stages:

- **Round II – Exploratory Data Analysis**
- **Round III – Data Visualization using Tableau**

---

## 📂 Dataset

The dataset contains food delivery trip information with the following attributes:

| Column | Description |
|---|---|
| `trip_id` | Unique ID of each delivery trip |
| `pickup_timestamp` | Date and time of pickup |
| `area` | Delivery area |
| `distance_km` | Delivery distance in kilometres |
| `traffic_condition` | Traffic condition during delivery |
| `delivery_time_min` | Actual delivery time in minutes |
| `promised_time_min` | Promised delivery time in minutes |

Original dataset size:

**123 rows × 7 columns**

---

# Round II – Exploratory Data Analysis

## 1. Data Loading and Inspection

The dataset was loaded using Python and Pandas.

The dataset shape, first five records, data types and missing values were inspected.

## 2. Data Cleaning

The following data preparation steps were performed:

- Checked for missing values.
- Checked pickup/GPS timestamps.
- Identified missing values in area, distance and traffic condition.
- Removed unrealistic distance values using the IQR method.
- Created distance bands for analysis.
- Created a delay indicator based on actual and promised delivery time.
- Created a delay status column.

After cleaning:

**116 rows × 10 columns**

No missing values remained in the cleaned dataset.

## 3. Outlier Detection

The Interquartile Range (IQR) method was used to identify unrealistic delivery distances.

The formula used was:

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR
Upper Bound = Q3 + 1.5 × IQR
Round 3:Visualising 
<img width="1017" height="596" alt="image" src="https://github.com/user-attachments/assets/96507995-d550-495e-873c-68f9101abc9f" />

