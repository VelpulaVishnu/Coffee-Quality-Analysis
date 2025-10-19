# ☕ CQI Capstone Project – Coffee Quality Analysis  

This project analyzes Arabica coffee quality data sourced from the Coffee Quality Institute (CQI).  
It focuses on understanding how attributes such as aroma, flavor, aftertaste, acidity, balance, and body influence overall coffee scores.  

### 🔗 [Live Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYjMwOTg3ODUtNGY1Yy00MGZhLTllOTEtMzcyZTE2NDA1ZGI5IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)


### Project Overview  
This project analyzes the **Arabica Coffee Quality dataset** from the **Coffee Quality Institute (CQI)** to uncover insights into coffee origins, processing methods, and sensory attributes.  
It includes **data cleaning, modeling, and visualization** using **Power BI and Excel**, helping identify top-performing regions, quality drivers, and defect patterns in coffee production.

---

## Business Objective  
The Coffee Quality Institute (CQI) is a non-profit organization that promotes global coffee quality standards.  
This project supports CQI’s mission by:  
- Understanding key sensory and physical factors influencing cup quality.  
- Identifying countries and processing methods that yield higher-quality coffee.  
- Reducing defects to enhance supply quality and profitability.

---

## Tools & Technologies  
- **Power BI** – Data modeling, visualization, and DAX calculations  
- **Microsoft Excel** – Data cleaning and preprocessing  
- **Power Query Editor** – Data transformation  
- **PowerPoint** – Presentation and storytelling  

---

## Data Preprocessing  
Performed entirely in **Excel and Power Query Editor**.  

Key steps:  
- **Column Standardization:** All column names converted to lowercase with underscores for consistency.  
- **Text Cleaning:** Trimmed spaces, removed special characters (e.g., “台灣咖啡研究室 → Taiwan Coffee Laboratory”).  
- **Type Corrections:** Converted ID columns to text; standardized lot numbers and harvest years.  
- **Missing Values:** Replaced nulls with "Unknown" or "not_available".  
- **Altitude Fix:** Split altitude ranges (e.g., “1200–1600”) and replaced outliers using median values.  
- **Bag Weight:** Removed "kg" text, replaced extreme values with standard weight (60kg).  
- **Processing Method & Variety:** Simplified naming (e.g., "Washed/Wet" → "Washed").  
- **Total Cup Points:** Recomputed from sensory attributes for better accuracy.

---

## Data Modeling  
Built a **Star Schema** model in Power BI for structured analysis.  

**Fact Table:**  
- `fact_coffee` → Aroma, Flavor, Aftertaste, Acidity, Body, Balance, Clean Cup, Sweetness, Total Cup Points, Defects, etc.  

**Dimension Tables:**  
- `dim_country` – Country and region data  
- `dim_processing_method` – Coffee processing techniques  
- `dim_variety` – Coffee bean varieties  
- `dim_color` – Bean color attributes  
- `dim_partner` – Partner or grading organizations  
- `dim_date` – Based on grading date for trend analysis  

This model supports flexible slicing by country, process, variety, or partner for detailed insights.

---

## 📈 Visualization Pages & Insights  

### **1️⃣ Executive Summary**
- **Dataset:** 207 coffee samples, 637 total recorded defects  
- **Average Cup Score:** 83.71 (Good quality but room for improvement)  
- **Defect Rate:** 65.7% of total weight defective  
- **Average Moisture:** 10.74% (within stable range)  
- **Top Countries:** Taiwan, Ethiopia, Guatemala, Tanzania, Madagascar  

<img src="https://github.com/VelpulaVishnu/Coffee-Quality-Analysis/blob/main/icons/Executive%20view%20Page.png" alt="Executive Summary Dashboard" width="800"/>

---

### **2️⃣ Sensory Attributes**
- Analyzed 10 core attributes — Aroma, Flavor, Aftertaste, Acidity, Body, Balance, Uniformity, Clean Cup, Sweetness, and Overall.  
- Clean Cup, Sweetness, and Uniformity achieved perfect scores (10/10).  
- Aroma (7.72), Flavor (7.74), Aftertaste (7.60) slightly lag behind.  
- Higher altitudes correlated with scores above 85.  
- Best methods: **Double Anaerobic, Semi-Washed, and Honey (Mossto)**.

<img src="https://github.com/VelpulaVishnu/Coffee-Quality-Analysis/blob/main/icons/Sensory%20Attributes%20Page.png" alt="Sensory Attributes Dashboard" width="800"/>

---

### **3️⃣ Origin and Defects Analysis**
- Total Coffee Weight: **1.59M kg**, with **1.41M kg (88.74%) defective**.  
- Usable coffee = only 179K kg.  
- Major defect sources: Guatemala, Honduras, Brazil.  
- **Defect categories:**  
  - Category 1: 28  
  - Category 2: 466  
  - Quakers: 143  
- Ethiopia & Myanmar showed 100% defect rates in some lots.

<img src="https://github.com/VelpulaVishnu/Coffee-Quality-Analysis/blob/main/icons/Defects%20and%20origins%20Page.png" alt="Origin and Defects Dashboard" width="800"/>

---

### **4️⃣ What-If Analysis**
- Scenario simulation for altitude and defect adjustments.  
- **Baseline Avg Score:** 83.71  
- **After adjustments:**  
  - What-If Avg Score = 83.77  
  - Altitude-adjusted Avg Score = 84.30  
  - Coffee saved (non-defective supply) = 423K kg  
  - Usable supply after adjustments = ~42.3% of total  

<img src="https://github.com/VelpulaVishnu/Coffee-Quality-Analysis/blob/main/icons/What%20if%20Analysis%20Page.png" alt="What-If Analysis Dashboard" width="800"/>

---

### **5️⃣ Insights Summary**
**Key Findings:**  
- **Top Sensory Drivers:** Aroma, Flavor, Acidity, Body, Balance.  
- **Top Varieties:** Castillo, Red Bourbon, Gesha, SL34+.  
- **Top Origins:** Ethiopia, Tanzania, Taiwan, Guatemala, Madagascar.  
- **Processing Influence:** Double Anaerobic, Honey, and Semi-Washed yielded the best results.  
- **Altitude Effect:** High-altitude coffees consistently scored higher (Avg ~85+).  
- **Defects Trend:** Most common in Washed and Natural processes; more frequent in March, April, and November grading dates.


## 💡 Suggestions

### 1️⃣ Improve Coffee Quality via Defect Reduction
- **Insight:** 58% of 2022 coffee weight was defective.  
- **Action:** Train farmers on harvesting & drying, invest in sorting/grading equipment, implement quality checkpoints.  
- **Impact:** 10% reduction in defects can save tens of thousands of kilos.

### 2️⃣ Promote Best-Performing Processing Methods
- **Insight:** Double Anaerobic, Honey (Mossto), Semi-Washed = best scores.  
- **Action:** Support adoption of these methods through training and case studies.  
- **Impact:** Improves average cup score without cutting supply.

### 3️⃣ Focus on High-Altitude Sourcing
- **Insight:** Coffees grown above 1500m scored ~84.4 vs baseline 83.9.  
- **Action:** Promote high-altitude sourcing and create “Altitude Grade” labeling.  
- **Impact:** Improves brand reputation and quality perception.

### 4️⃣ Origin-Based Strategies
- **Insight:** Certain origins show extreme defect or excellence levels.  
- **Action:**  
  - For high-defect regions: provide training & infrastructure support.  
  - For top-performing regions: highlight in marketing campaigns.  
- **Impact:** Strengthens CQI’s position as a global quality leader.

---

## Learning Outcomes  
- Hands-on practice in **data cleaning, transformation, and modeling**.  
- Built a fully interactive Power BI dashboard from scratch.  
- Learned **DAX, performance optimization, and relationship-based design**.  
- Derived actionable business insights from agricultural data.  

---

## Conclusion  
The CQI Coffee Quality Analysis project demonstrates how data-driven insights can improve coffee grading accuracy, minimize defects, and enhance global coffee quality.  
Through data modeling and visualization, it provides a framework for improving decision-making in the specialty coffee industry.

---

☕ *“Behind every successful analyst is a substantial amount of coffee.”*  
— Vishnu
