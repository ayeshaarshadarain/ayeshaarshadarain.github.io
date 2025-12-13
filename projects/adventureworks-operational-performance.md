# AdventureWorks BI Project  
## Understanding Sales Demand and Production Bottlenecks

**Tools:** SQL Server (SSMS), Power BI, DAX  
**Focus:** Sales trends, production efficiency, operational bottlenecks

---

## Why I Did This Project

As part of my learning journey in Business Intelligence, I wanted to understand how **sales demand, production performance, and quality issues** connect in a real business setting.

Rather than looking at dashboards in isolation, I focused on one main question:

**Where is the business losing revenue, and what operational issues might be causing it?**

To explore this, I looked at two areas:
- Sales performance and demand behavior  
- Production and quality performance  

---

## How I Prepared the Data (SQL → Power BI)

Before working in Power BI, I spent most of my time in **SQL Server Management Studio**. I wanted to avoid fixing data problems later inside Power BI.

Using SQL, I:
- Explored the AdventureWorksDW tables to understand what data was useful
- Created SQL views to clean and simplify the data
- Removed unnecessary columns and duplicate keys
- Standardized date fields
- Aggregated data (e.g., monthly sales trends)

Key views included:
- Sales data
- Work order and production data
- Monthly sales summary
- Product and date dimensions

---

## Data Modeling in Power BI

In Power BI, I built a **star-schema style model**, which was a key learning goal.

- Sales and production tables act as fact tables  
- Product and date tables act as dimensions  
- Single-direction relationships from dimensions to facts  
- A shared date table connects sales and production  

I also created DAX measures for:
- Year-over-year and month-over-month changes  
- Scrap rate  
- Production efficiency  

---

## What I Learned from the Sales Dashboard

Some key observations:
- **Bikes account for about 86% of total revenue**
- Revenue is heavily concentrated in one category
- Strong **seasonal demand patterns** exist (spring and Q4 peaks)

I also noticed that:
- Some months show extreme YoY percentage changes due to low prior-year values
- Some products sell many units but generate limited revenue, while others generate high revenue with lower volume

This helped me better understand pricing and product mix effects.

---

## What I Learned from the Production & Quality Dashboard

Although production efficiency appears high overall, deeper analysis showed:

- Scrap rate spikes in certain months, indicating quality issues
- Average manufacturing cycle time is around **13 days**
- Many high-demand products are underproduced relative to safety stock levels

Category-level analysis showed that components tend to have higher scrap rates, while accessories are more stable.

---

## Why I Did Not Include Inventory Analysis

I initially planned to include inventory analysis, but AdventureWorks inventory data mixes:
- Raw materials  
- Components  
- Hardware items  

This makes finished-goods inventory analysis unreliable.

Rather than forcing misleading insights, I focused on **sales and operations**, where the data supports clearer conclusions.

---

## Putting Everything Together

The dashboards suggest that:
- Demand is seasonal and volatile
- Production struggles to adjust smoothly
- Quality issues reduce available output
- Underproduction leads to missed sales opportunities

---

## What This Project Taught Me

This project helped me understand that Business Intelligence is not just about visuals, but about:
- Asking the right questions  
- Preparing data carefully  
- Modeling relationships correctly  
- Interpreting results critically  

It strengthened my understanding of how operational decisions affect revenue and how BI can reveal those connections.
