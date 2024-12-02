# Hotel Management Dashboard Report

## **Project Overview**
The **Hotel Management Dashboard** project aims to provide actionable insights into hotel performance using **Power BI**. This project analyzes key metrics such as occupancy rates, revenue trends, booking patterns, and cancellations to enable data-driven decision-making for hotel managers.

---

## **Project Objectives**
1. **Optimize Occupancy**: Identify trends in room utilization and increase occupancy rates.
2. **Boost Revenue**: Analyze revenue by customer type, booking channel, and geography.
3. **Understand Cancellations**: Track cancellation trends and their impact on revenue.
4. **Identify High-Performing Segments**: Understand the contribution of customer segments and geographical markets.

---

## **Dataset and Cleaning Process**

### Dataset Overview
The raw dataset contains **119,390 rows** and **31 columns**, with fields such as:
- **Booking Details**: `Arrival Date`, `Room Type`, `Market Segment`.
- **Customer Demographics**: `Country`, `Customer Type`.
- **Performance Metrics**: `Adr` (Average Daily Rate), `Revenue`, `Cancellation`.

### Data Cleaning Steps
1. **Handled Missing Values**:
   - Replaced missing `Country` values with "Unknown".
   - Imputed `Agent` and `Company` with "Not Specified" or excluded them due to insufficient data.
2. **Fixed Data Types**:
   - Converted `Arrival Date` to `datetime` format for time-based analysis.
   - Changed boolean-like fields (`Is Canceled`, `Is Repeated Guest`) to actual Boolean data type.
3. **Removed Outliers**:
   - Eliminated negative values in `Adr`, ensuring accurate revenue analysis.
4. **Added Derived Metrics**:
   - `Total Revenue` = `Adr` × `Total Days`.
   - `Booking Length` = `Stays In Week Nights` + `Stays In Weekend Nights`.

---

## **Data Modeling**
Data was modeled in **Power BI** using a **Star Schema**:
- **Fact Table**:
  - `hotel_data`: Contains booking details, performance metrics, and derived measures.
- **Dimension Tables**:
  - **Date Table**: Enables slicing data by day, week, month, and quarter.
  - **Room Types**: Groups assigned room types for better analysis.
  - **Customer Segments**: Groups customers by type (e.g., transient, corporate).
- Relationships:
  - Linked `hotel_data` to `Date Table` using `Arrival Date`.
  - Created slicers for `Country`, `Market Segment`, and `Customer Type`.

---

## **Power BI Development**
### Key Visualizations:
1. **Overview Dashboard**:
   - Displays total revenue, occupancy trends, and top-performing market segments.
   - Filters for `Country`, `Hotel Type`, and `Booking Period`.

2. **KPI Dashboard**:
   - Highlights key metrics:
     - **Occupancy Rate**: ~3.43%
     - **ADR**: $101.83
     - **RevPAR**: $104.40
     - **Cancellation Rate**: 37.04%
   - Tracks weeknight vs. weekend performance.

3. **Geographical Dashboard**:
   - Maps top-performing countries:
     - **Portugal**: $14.13M
     - **Great Britain**: $5.28M
     - **France**: $4.03M.

### Advanced Features:
- **DAX Measures**:
  - `Occupancy Rate` = `(Total Days / Total Rooms) * 100`.
  - `RevPAR` = `Total Revenue / Total Rooms Available`.
  - `Cancellation Rate` = `(Total Cancellations / Total Bookings) * 100`.
- **Dynamic Filters**:
  - Slicers for customer type, booking channel, and time periods.
- **Conditional Formatting**:
  - Highlighted low-performing weeks in grey and high-performing ones in bold colors.

---

## **Insights and Business Questions**

### Insights:
1. **Weeknight vs. Weekend Performance**:
   - Weeknight Revenue: **$31.15M**
   - Weekend Revenue: **$11.57M**
   - Weeknights outperform weekends significantly.
2. **Top Customer Segments**:
   - **Transient Customers**: Contribute **$34.20M**, dominating revenue.
   - **Transient-Party**: $6.54M.
3. **Cancellations**:
   - High cancellation rate (**37.04%**) impacts revenue planning.
   - **44,224 cancellations** in total.
4. **Geographical Revenue**:
   - **Portugal** leads with $14.13M in revenue, followed by Great Britain and France.

### Business Questions Addressed:
1. **How does occupancy fluctuate over time?**
   - Answer: Occupancy is consistent across weekdays but dips on weekends.
2. **Which segments drive the most revenue?**
   - Answer: Transient customers dominate, contributing over 70% of total revenue.
3. **What are the trends in cancellations?**
   - Answer: Cancellations follow a seasonal pattern, peaking during high-demand periods.
4. **Which countries are most profitable?**
   - Answer: Portugal, Great Britain, and France are top contributors.

---

## **Conclusion**
This dashboard empowers hotel managers to:
- Optimize pricing strategies using ADR and RevPAR trends.
- Focus marketing efforts on high-revenue segments like transient customers and specific countries.
- Address cancellations to minimize revenue loss.

---

## **How to Access**
1. **Live Dashboard**:  
   Access the interactive dashboard [here](https://app.powerbi.com/reportEmbed?reportId=5de85a79-0224-4844-8e58-b87380bcfa42&autoAuth=true&ctid=e9b87214-8e8f-4ad0-90ec-9d5c56c94931).

2. **Power BI File**:  
   Open the `Hotel_Report.pbix` file in the `power_bi` folder.

---

## **Future Work**
- Incorporate predictive analytics for demand forecasting.
- Perform deeper analysis of cancellations by segment and geography.
- Integrate external data for enhanced insights (e.g., weather, local events).

---
