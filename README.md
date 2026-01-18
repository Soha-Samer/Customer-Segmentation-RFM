# Customer Segmentation & RFM Analysis 📊

**Tools:** Python (Pandas), Power BI, SQL
**Dataset:** [UCI Online Retail Data](https://archive.ics.uci.edu/ml/datasets/online+retail) (500k+ Transactions)

### 🚀 Business Overview
In the competitive e-commerce landscape, treating every customer the same is a waste of marketing budget. This project analyzes **541,909 raw transaction records** to identify customer segments and optimize retention strategies.

Using the **RFM (Recency, Frequency, Monetary)** methodology, I segmented the user base to answer:
* *Who are our high-value "Champions"?*
* *Which loyal users are at risk of churning?*
* *How can we increase the Average Order Value (AOV)?*

### 💡 Key Insights (The 80/20 Rule)
* **Champions (21% of users)** generate **68% of Total Revenue**.
    * *Strategy:* Implement a VIP Loyalty Program/Early Access.
* **At-Risk Loyalists:** A significant cluster of high-spenders hasn't purchased in **90+ days**.
    * *Strategy:* Launch automated "We Miss You" email campaigns with time-limited discounts.
* **Hibernating:** 30% of users are low-frequency, low-recency.
    * *Strategy:* Stop expensive ad spend on this group to optimize ROI.

### 🛠 Technical Implementation
* **Data Cleaning (Python):** * Removed cancelled orders (Invoice `C...`) and cleaned 130,000+ missing User IDs.
    * Engineered `TotalAmount` features and handled negative quantity errors.
* **RFM Engine:**
    * Calculated Recency (Days since last purchase), Frequency (Count of orders), and Monetary value.
    * Applied **Quantile Scoring (1-5)** to rank customers relative to the population.
* **Segmentation Logic:**
    * Used **Regex Mapping** to assign human-readable labels (e.g., `555` -> "Champion", `111` -> "Hibernating").

### 📊 Dashboard
*(See `DashboardRFM.png` for the full interactive view)*

---
*Created by [Soha Elasnary] - Data Analyst*
