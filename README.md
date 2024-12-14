# **Car Accidents Insights**
### Based on Kaggle's *"US Accidents (2016 - 2023)"* Dataset

![Motorcycle Accident](https://gutierrezinjury.attorney/wp-content/uploads/2021/01/motorcycle-accidents_lg-1gggg.jpg)

---

## **Dataset Overview**
The dataset, titled *"US_Accidents_March23.csv"*, contains information about car accidents across the United States up to **March 2023**. The data includes:
- **Location details**: City, state, and coordinates.
- **Accident details**: Severity, start and end times.
- **Environmental features**: Weather, road conditions, and more.

---

## **Objective**
The primary goals of this project are:
1. **Clean** and preprocess the dataset for analysis.
2. Sample a subset of **10,000 rows** for quick exploration.
3. Ensure **datetime consistency** for time-related columns (*Start_Time* and *End_Time*).
4. Perform initial analysis to highlight accident trends.

---

## **Steps Undertaken**

### 1️⃣ **Data Loading**
The dataset was loaded into a pandas DataFrame:
```python
import pandas as pd
file_path = r"US_Accidents_March23.csv"
df = pd.read_csv(file_path)
```

---

### 2️⃣ **Cleaning Missing Values**
To ensure clean and reliable data:
- Rows with missing (NA) values were dropped:
```python
df_no_na = df.dropna()
```
This step ensures that **only complete rows** are used for analysis.

---

### 3️⃣ **Sampling 10,000 Rows**
From the cleaned dataset, a random sample of 10,000 rows was selected:
```python
cleaned_accidents = df_no_na.sample(n=10000, random_state=42)
```
- `random_state=42` ensures **reproducibility** of the sample.

---

### 4️⃣ **Datetime Conversion**
Columns *Start_Time* and *End_Time* were converted to datetime format:
```python
cleaned_accidents['Start_Time'] = pd.to_datetime(cleaned_accidents['Start_Time'])
cleaned_accidents['End_Time'] = pd.to_datetime(cleaned_accidents['End_Time'])
```
This step ensures accurate handling of **date and time values** for trend analysis.

---

### 5️⃣ **Exporting the Cleaned Sample**
The cleaned dataset was saved for further use:
```python
output_path = r"C:\Users\vange\Desktop\github project\cleaned_accidents.csv"
cleaned_accidents.to_csv(output_path, index=False)
```
- The cleaned file is saved at: **`C:\Users\vange\Desktop\github project\cleaned_accidents.csv`**

---

## **Team Members**
This project was a collaborative effort by:
- **Georgios Birmpakos**
- **Vasileios Katsikas**
- **Evangelos Diaskoufis**

---

## **Questionnaire Highlights**

### 📝 **Key Areas of Focus**

#### **A. Accidents Per State**
- **Objective**: Identify the states with the **highest** and **lowest** accident counts.
- **Insights**: Highlight accident trends across states.

#### **B. Most Prone State for Accidents**
- Determine the **state with the highest accident frequency**.
- Analyze if there's a significant gap compared to other states.

#### **C. Accidents Per Month**
- **Goal**: Examine seasonal trends in accidents.
- Identify peak months where accidents are most common.

#### **D. Accidents Near Specific Locations**
- Analyze accidents near:
  - **Junctions**
  - **Stop signs**
  - **Traffic signals**
- Calculate the **percentage** of total accidents occurring in these areas.

---

## **Next Steps**

### 🔍 **Exploratory Data Analysis (EDA)**
1. **Accident Severity Analysis**:
   - Explore severity distribution across **cities** and **states**.
   - Identify the most dangerous areas based on accident severity.

2. **Temporal and Spatial Trends**:
   - Locate **geographical hotspots** for accidents.
   - Analyze **time-based trends**:
     - Peak accident **hours**
     - Seasonal patterns (e.g., months or holidays).

---

## **Summary**
This documentation outlines the key steps in cleaning and preparing the *"US Accidents"* dataset for analysis. The cleaned dataset, containing 10,000 sampled rows, is now ready for:
- **Deeper analysis** of accident severity and trends.
- **Visualization** of hotspots, time-based patterns, and critical accident locations.

---

**Stay tuned for further insights and visualizations!** 🚗💥

---

![Road Safety Image](https://static.wixstatic.com/media/ae4bd2_e0d66e5dc94c438e807cc0db43028297~mv2.webp/v1/fill/w_640,h_428,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ae4bd2_e0d66e5dc94c438e807cc0db43028297~mv2.webp)


