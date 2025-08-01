# TRADE-of-GOODS
# 🌍 Global Trade Data Analysis & Power BI Dashboard

Course:INSY 8413 -Introduction to Big Data Analysis
Academic Year:2024-2025
Stundent name:Ishimwe Amos
ID:26247
Instructor: Eric Maniraguha
Dataset source:Trading of Goods

## 📌 Project Overview
This project analyzes global trade data to uncover key insights into trade value, weight, and trends across countries, years, and commodities.  

It combines **Python** for data cleaning, exploratory analysis, and predictive modeling with a **Power BI dashboard** for interactive data visualization.  

The goal is to provide clear insights into:
- 📊 Trade performance across countries
- 📈 Import vs Export distribution
- 📅 Trade trends over time
- 🔮 Predictive modeling of trade values

---

## 📂 Dataset Information
- **Rows:** 5,728  
- **Columns:** 9  

| Column Name       | Description                                 |
|-------------------|---------------------------------------------|
| Country or Area   | Name of the country or region              |
| Year              | Year of the trade record                   |
| Commodity         | Traded product or commodity               |
| Flow              | Import or Export indicator                |
| Trade (USD)       | Trade value in US dollars                 |
| Weight (kg)       | Weight of traded goods                    |
| Quantity Name     | Type of quantity measurement              |
| Quantity          | Quantity of items                         |
| Flow_Code         | Numeric code for Import (0) or Export (1) |

---

## 🛠 Data Cleaning Process (Python)
1. Loaded dataset using **Pandas**.   <img width="804" height="632" alt="b data load and clean data" src="https://github.com/user-attachments/assets/d0eb9f07-152a-44ba-8aa6-a9e6af355f99" />

2. Filled missing values in `Quantity` with 0.  
3. Converted `Trade (USD)` and `Weight (kg)` to numeric values.  
4. Created a new column `Flow_Code` (0 = Import, 1 = Export).  
5. Dropped rows with missing `Trade (USD)`.  
6. Exported the cleaned dataset to **`cleaned_trade_data.csv`** for Power BI.  <img width="660" height="276" alt="cleaning data 1" src="https://github.com/user-attachments/assets/1a081de6-5907-4175-8668-fa45a9e5107a" />


---

## 🤖 Machine Learning Model
A **Linear Regression model** was trained to predict `Trade (USD)` using:  
- `Year`  
- `Weight (kg)`  
- `Flow_Code`


### 🔹 Model Evaluation Results
- **RMSE:** 478,248,936.32  
- **R² Score:** 0.0370  

Predictions were exported to **`predictions.csv`** for Power BI visualization.

---

## 📊 Power BI Dashboard
<img width="1179" height="666" alt="power bi" src="https://github.com/user-attachments/assets/79966248-4e36-4b08-9c87-53ca8d8cf9cd" />

### Dashboard Features:
✅ **World Map** – Trade distribution by country  <img width="1370" height="794" alt="worl map and codes" src="https://github.com/user-attachments/assets/892506e7-18c0-4b7d-b101-f9bb88f97513" />

✅ **Pie Chart** – Trade share by flow (Import/Export)  <img width="1083" height="827" alt="pichart" src="https://github.com/user-attachments/assets/cf636129-93cd-4469-a148-f99909a27bbe" />

✅ **KPI Cards** – Total trade value and total weight traded  <img width="1043" height="819" alt="weight traded" src="https://github.com/user-attachments/assets/63b2806c-dacd-45c4-88ce-9a7cca58ec12" />

✅ **Bar Chart** – Total trade by top countries  <img width="616" height="164" alt="total trade" src="https://github.com/user-attachments/assets/fef00692-d216-4e7c-a10e-f9572c03a37f" />
<img width="1152" height="584" alt="total trade top country" src="https://github.com/user-attachments/assets/f7dbd765-00cb-4a09-9cf1-5dadb846d603" />


✅ **Column Chart** – Weight traded by year  <img width="1043" height="819" alt="weight traded" src="https://github.com/user-attachments/assets/31a362a2-5c9b-46fd-8310-b9411daac609" />

✅ **Line Chart** – Trade value trends over time   <img width="979" height="509" alt="trade value diagram" src="https://github.com/user-attachments/assets/c4f0c065-4ae3-4ef1-aea5-4e627e1fb991" />


### Interactivity:
- Slicers for **Year, Country, Flow, and Commodity**  
- Drill-down options on bar and column charts  
- Tooltips for additional context  

---

## 📌 Key Insights
- 🌍 Trade value is concentrated in a few major countries (EU-28, Italy, Germany).  
- 📈 Imports and exports show fluctuating trends with growth in recent years.  
- 📦 Certain commodities dominate trade value compared to others.  

The **Power BI dashboard** provides an interactive way to explore trade data by year, country, and flow type.

---

## 🚀 How to Use This Project
### 🔹 Steps to Reproduce
1. **Run the Python script** to clean and process the dataset.  
2. The script will generate:
   - `output/cleaned_trade_data.csv` – Cleaned dataset
   - `output/predictions.csv` – Model predictions
3. **Open Power BI Desktop.**
4. Load the two CSV files into Power BI.  
5. Use the dashboard to explore insights using filters, slicers, and drill-downs.

---

## 📁 Project Structure

