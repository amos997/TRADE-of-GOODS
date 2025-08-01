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
6. Exported the cleaned dataset to **`cleaned_trade_data.csv`** for Power BI.  

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
### Dashboard Features:
✅ **World Map** – Trade distribution by country  
✅ **Pie Chart** – Trade share by flow (Import/Export)  
✅ **KPI Cards** – Total trade value and total weight traded  
✅ **Bar Chart** – Total trade by top countries  
✅ **Column Chart** – Weight traded by year  
✅ **Line Chart** – Trade value trends over time  

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

