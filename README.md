# Delhivery_Analysis
Analyzing Delhivery’s logistics data to uncover shipment trends, evaluate delivery performance, and identify factors affecting delivery times. The project aims to improve delivery estimates, optimize shipping methods (FTL and Carting), and identify high-traffic regions that may need better hub capacity.


# Delhivery Logistics Data Analysis

##  Project Overview

This project focuses on analyzing Delhivery's logistics dataset to understand shipment patterns, delivery performance, and operational trends across India.

Using Python, statistical techniques, hypothesis testing, and feature engineering, the project explores shipment data to uncover meaningful patterns and generate actionable insights that can support better logistics and business decisions.

##  Project Objectives

- Understand shipment patterns and delivery trends across India.
- Clean, preprocess, and transform raw logistics data.
- Analyze estimated versus actual delivery times.
- Evaluate transportation methods such as FTL and Carting.
- Identify high-traffic regions and frequently used routes.
- Explore factors contributing to delivery delays and operational inefficiencies.

## 🔍 Analysis Performed

- **Data Cleaning & Preprocessing:** Handling missing values, duplicates, inconsistent records, and data type conversions.
- **Exploratory Data Analysis (EDA):** Univariate and multivariate analysis to understand shipment patterns and relationships.
- **Statistical Analysis:** Applying descriptive statistics and probability concepts to understand data distributions and trends.
- **Hypothesis Testing:** Testing business assumptions and identifying statistically significant differences or relationships.
- **Feature Engineering:** Creating and transforming relevant features to extract additional information from the existing data.
- **Data Visualization:** Using Matplotlib and Seaborn to communicate trends, patterns, and analytical findings.

## Key Business Insights

### 1. Major States Dominate Shipment Activity

Haryana, Maharashtra, and Karnataka consistently rank among the top source and destination states. This indicates that these regions play a significant role in both generating and receiving shipments, making them important areas for potential hub expansion and infrastructure investment.

### 2. A Small Number of Corridors Drive Significant Trip Volume

Certain routes account for a disproportionate share of total trips, particularly within the Bangalore hub network. For example, Bangalore Nellamangala to Bengaluru KG Airport Hub records 151 trips. Some high-frequency routes also involve movements within the same hub, indicating substantial local redistribution activity.

### 3. Busy Corridors Have Different Operational Requirements

Bangalore's busiest corridors generally involve shorter trips, averaging less than 90 minutes and 30 km. In contrast, selected Chandigarh and Bhiwandi corridors show average durations of approximately 240–340 minutes. This suggests that operational delays or hub-level processing may need investigation rather than simply increasing vehicle availability.

### 4. FTL Demonstrates Better Distance-Based Efficiency Than Carting

- **FTL:** Average distance of approximately 147.5 km, completed in 317 minutes, with an effective speed of around 27.9 km/hr.
- **Carting:** Average distance of approximately 40 km, completed in 118 minutes, with an effective speed of around 20.3 km/hr.

FTL demonstrates better average distance-based speed despite covering longer distances. This supports using FTL for longer routes and Carting for shorter, localized deliveries.

### 5. OSRM Underestimates Actual Delivery Time

The analysis reveals that OSRM-based estimated travel time is approximately 195 minutes lower than actual delivery time on average. The gap also increases on longer routes, indicating that raw routing estimates may not fully account for real-world operational conditions.

This could lead to unrealistic customer-facing delivery promises if OSRM estimates are used without calibration.

### 6. Internal Operational Tracking Provides a Reliable Foundation

The average difference between `actual_time` and `segment_actual_time` is approximately 3 minutes. This close agreement suggests that Delhivery's internal scan-based tracking data can serve as a strong foundation for future delivery-time forecasting models.

OSRM estimates can be retained as supplementary routing information rather than treated as the primary source of actual delivery duration.

## Business Recommendations

### 1. Recalibrate Customer-Facing Delivery Time Estimates

- **Action:** Introduce correction factors into OSRM-based delivery estimates using historical delivery performance.
- **Reason:** Actual delivery time exceeds OSRM estimates by approximately 195 minutes on average, with larger differences on longer routes.
- **Expected Impact:** More realistic delivery promises, improved customer experience, and potentially fewer delivery-time-related support queries.

### 2. Prioritize Hub Investment in High-Demand Regions

- **Action:** Focus additional hub capacity and staffing on regions generating and receiving the highest shipment volumes.
- **Reason:** Haryana, Maharashtra, and Karnataka consistently appear among the leading source and destination states.
- **Expected Impact:** Better utilization of infrastructure investments and improved network efficiency.

### 3. Optimize High-Frequency Delivery Corridors

- **Action:** Introduce dedicated vehicle allocation, priority scheduling, and optimized routing for high-volume corridors.
- **Reason:** A relatively small number of routes account for a significant share of total trips.
- **Expected Impact:** Even small improvements on these routes could generate meaningful network-wide operational gains.

### 4. Match Transportation Methods to Route Distance

- **Action:** Prioritize FTL for longer-distance shipments and use Carting for shorter, localized deliveries.
- **Reason:** FTL demonstrates better average distance-based efficiency compared to Carting in the analyzed dataset.
- **Expected Impact:** Better transportation resource utilization and improved delivery efficiency without necessarily increasing fleet capacity.

### 5. Standardize Trip-Time and Distance Measurement

- **Action:** Establish consistent definitions for trip-level and segment-level time and distance calculations. Use trip-level OSRM measurements as a standardized routing reference while retaining internal actual-time records as the operational source of truth.
- **Reason:** Segment-summed figures can differ from trip-level calculations, particularly on longer journeys, creating inconsistencies across reports and analysis.
- **Expected Impact:** More consistent operational reporting, reliable comparisons, and a stronger foundation for future forecasting models.

## 🛠️ Tools & Technologies

- **Python** – Data analysis and processing
- **NumPy** – Numerical computations
- **Pandas** – Data manipulation and preprocessing
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical data visualization
- **Statistics** – Descriptive and inferential analysis
- **Hypothesis Testing** – Statistical validation of business assumptions
- **Feature Engineering** – Feature creation and transformation
- **Jupyter Notebook** – Development and analysis environment

## 🚀 Conclusion

This project demonstrates how data cleaning, exploratory data analysis, statistical techniques, hypothesis testing, and feature engineering can be applied to real-world logistics challenges.

By identifying high-demand regions, evaluating transportation efficiency, analyzing delivery-time estimation gaps, and understanding operational patterns, the project translates raw shipment data into actionable business insights.

The ultimate objective is to support data-driven decisions that improve delivery estimates, optimize transportation operations, and strengthen logistics network efficiency.

---

**Project Domain:** Logistics & Supply Chain Analytics

**Project Type:** Exploratory Data Analysis | Statistical Analysis | Hypothesis Testing | Feature Engineering
