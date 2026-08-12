# ☕ Coffee Sales Analytics & Performance Dashboard

## 📌 Executive Summary
This project delivers an interactive, data-driven sales analysis dashboard for a coffee shop operation using **Microsoft Excel** and **Power Pivot**. By analyzing sales records, item pricing, payment preference trends, and order fulfillment locations (In-store vs. Takeaway), the dashboard translates transactional logs into strategic business intelligence.

---

## 📸 Dashboard & Project Screenshots

### 📊 Interactive Dashboard View
![Dashboard View](Screenshot%202026-08-12%20102229.png)

**Description & Key Highlights:**
* **Executive Summary (KPIs):** Displays overall high-level performance metrics:
  * **Total Sales:** `$141,713.50`
  * **Total Orders / Transactions:** `14,928`
* **Interactive Slicers:** Positioned on the left panel, allowing users to dynamically filter data by **Item**, **Payment Method**, and **Location**, alongside a **Timeline Filter** for date selection.
* **Visual Insights:**
  * **Sales Per Month (Line Chart):** Tracks monthly revenue trends throughout 2023, showing steady performance with peak periods in June (`$12,228.00`) and December (`$12,266.00`).
  * **Top Items (Bar Chart):** Ranks menu offerings based on total revenue generated.
  * **Top Payment Method (Donut Chart):** Visualizes the breakdown across Credit Card, Digital Wallet, and Cash payments.
  * **Top Location (Horizontal Bar Chart):** Compares total order volume between **In-store** and **Takeaway** fulfillment.

---

### 🛠️ Data Modeling & Relationships (Power Pivot)
![Data Model](Screenshot%202026-08-12%20102243.png)

**Description & Model Architecture:**
* **Data Schema:** Built a Relational Data Model connecting lookup tables with core transactional logs inside **Power Pivot**.
* **Table Relationships:**
  * **`Data` (Fact Table):** Contains transactional-level logs (`Transaction ID`, `Item`, `Quantity`, `Price Per Unit`, `Total Spent`, `Payment Method`, `Location`, `Transaction Date`).
  * **`Item Price` (Dimension Table):** Contains catalog item pricing (`Item`, `Price Per Unit`).
  * Connected via a **1-to-Many (1:*)** relationship using the `Item` field.
* **Benefit:** Ensures data integrity, reduces data redundancy, and enables smooth aggregation across dynamic Excel calculations.

---

### 📋 Catalog Pricing & Data Tables

#### 🏷️ Item Pricing Lookup Table
![Item Price Table](Screenshot%202026-08-12%20102216.png)

**Description & Master Catalog:**
* Standardized base pricing table utilized inside the data model:
  * **Salad:** `$5.00` | **Sandwich / Smoothie:** `$4.00` | **Cake / Juice:** `$3.00`
  * **Coffee:** `$2.00` | **Tea:** `$1.50` | **Cookie:** `$1.00`

#### 📦 Transactional Fact Table
![Data Table Sheet](Screenshot%202026-08-12%20102222.png)

**Description & Transaction Records:**
* Operational transactional database capturing individual line items, quantities purchased, line item total values (`Total Spent`), transaction timestamps, payment fulfillment methods, and store locations.

---

### 📈 Pivot Tables & Granular Insights Breakdown
![Insights Analysis Sheet](Screenshot%202026-08-12%20102233.png)

**Description & Analytical Findings:**
* **Revenue Drivers:** **Smoothie** and **Sandwich** lead sales, each bringing in **$29,756.00**, followed by **Cake** and **Juice** (**$23,157.00** each).
* **Volume Analysis:** A total of **45,240 items** were sold. **Cake** and **Juice** saw the highest volume with **7,719 units** sold each.
* **Fulfillment Channels:** Revenue is split almost 50/50 between **In-store** (**$71,479.00**) and **Takeaway** (**$70,234.50**).
* **Payment Method Preferences:** **Credit Card** represents the primary payment method (**$47,763.00**), followed by **Digital Wallet** (**$47,351.00**) and **Cash** (**$46,599.50**).
