# **Hotel Performance Insights Dashboard**

## **Overview**
The **Hotel Performance Insights Dashboard** is an advanced analytics project built with **Power BI** to help hotel managers make data-driven decisions. This interactive dashboard provides actionable insights into key performance metrics, including occupancy rates, revenue trends, booking patterns, and cancellations, enabling better operational and strategic decision-making.

### **Live Dashboard**
🌟 **[Explore the Interactive Dashboard](https://app.powerbi.com/reportEmbed?reportId=5de85a79-0224-4844-8e58-b87380bcfa42&autoAuth=true&ctid=e9b87214-8e8f-4ad0-90ec-9d5c56c94931)** 🌟

---

## **Purpose**
Hotels generate vast amounts of data daily, yet turning this data into insights can be challenging. This dashboard addresses this gap by:
1. Optimizing **occupancy rates** through trend analysis.
2. Improving **revenue** using Average Daily Rate (ADR) and Revenue Per Available Room (RevPAR).
3. Analyzing **booking patterns** for weekdays vs. weekends.
4. Understanding **cancellation trends** to mitigate revenue loss.
5. Identifying high-revenue **customer segments** and **geographies**.

---

## **Key Features**
- **Advanced Data Cleaning**:
  - Handled missing values and removed outliers.
  - Derived new metrics like `Total Revenue` and `Booking Length`.
- **Data Modeling**:
  - Implemented a **Star Schema** with a fact table (`hotel_data`) and dimensions (`Date Table`, `Customer Segments`, `Room Types`).
- **Advanced DAX Calculations**:
  - Created measures for **Occupancy Rate**, **RevPAR**, and **Cancellation Rate**.
- **Dynamic Visualizations**:
  - Filters for customer type, market segment, country, and time period.
  - Conditional formatting for high- and low-performing weeks.
- **Interactive Geographical Analysis**:
  - Mapped top-performing countries by revenue.

---

## **Business Questions Answered**
1. **How does occupancy fluctuate over time?**
   - Occupancy rates remain consistent on weekdays but drop on weekends.
2. **Which segments drive the most revenue?**
   - **Transient customers** contribute over 70% of total revenue.
3. **What are the trends in cancellations?**
   - High cancellation rates (**37.04%**) occur during peak seasons.
4. **Which countries generate the most revenue?**
   - **Portugal**, **Great Britain**, and **France** lead in revenue contribution.

---

## **Key Insights**
- **Weeknight Revenue**: $31.15M  
- **Weekend Revenue**: $11.57M  
  → Weeknights generate nearly 3x the revenue of weekends.
  
- **Top 3 Revenue-Generating Countries**:
  1. **Portugal**: $14.13M
  2. **Great Britain**: $5.28M
  3. **France**: $4.03M

- **High Cancellation Rate**: 37.04% (44,224 bookings canceled).  
  → Suggests the need for improved cancellation policies.

---

## **Project Workflow**
1. **Data Cleaning**:
   - Replaced missing values (`Country` as "Unknown").
   - Converted date fields and removed negative ADR outliers.
2. **Data Modeling**:
   - Designed relationships between fact and dimension tables in Power BI.
3. **DAX Calculations**:
   - Created metrics like ADR, RevPAR, Occupancy Rate, and Cancellation Rate.
4. **Dashboard Development**:
   - Designed dynamic, interactive visuals for trend analysis and geographical insights.

---

## **Tools and Technologies**
- **Power BI**: For data visualization and interactive dashboard creation.
- **DAX (Data Analysis Expressions)**: To calculate advanced metrics.
- **Python (Pandas)**: For data cleaning and preprocessing.

---