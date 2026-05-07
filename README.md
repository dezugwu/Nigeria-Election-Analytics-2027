# 🇳🇬 Nigeria Election Analytics 2027

## 📌 Project Overview
This project focuses on building a real-time data analytics system to track and analyze the popularity of potential presidential candidates ahead of Nigeria's 2027 elections.

The goal is to move beyond opinions and media narratives by using data to uncover trends in public interest and engagement.

---

## 🎯 Objectives
- Identify the Top 10 most discussed political candidates
- Track popularity trends over time (April 2026 – February 2027)
- Measure engagement across digital platforms
- Develop a custom Popularity Score for ranking candidates
- Visualize insights using Power BI

---

## 📊 Data Sources
- YouTube (video engagement data)
- Google Trends (search interest)

---

## ⚙️ Tools & Technologies
- Python (data extraction & processing)
- SQL (SQLite for data storage & querying)
- Power BI (data visualization)
- APIs (YouTube Data API)
- Google Trends (manual export + processing)

---

## 🧱 Project Status
🚧 In Progress (Day 4 — Multi-Source Data Integration Completed)

---

## 🧱 Data Architecture

The project follows a structured data modeling approach:

### Fact Tables
- `fact_social_media` → Social media engagement data (YouTube)
- `fact_trends` → Search interest data (Google Trends)

### Dimension Tables
- `dim_candidates`
- `dim_date`
- `dim_platform`

This structure ensures scalability and supports advanced analytics such as trend analysis, growth tracking, and candidate comparison.

---

## 📊 Data Collection

Datasets have been extracted from multiple sources:

### YouTube Data
- Video titles
- Views, likes, comments
- Engagement metrics
- Published date

### Google Trends Data
- Search interest over time
- Candidate-level trend scores
- Nigeria-specific filtering

---

## 🧹 Data Cleaning & Transformation

- Removed duplicates and handled missing values  
- Converted date fields to proper datetime formats  
- Engineered new features (year, month, engagement rate)  
- Restructured Google Trends data (wide → long format)  
- Standardized schema across datasets for integration  

---

## 🗄️ Data Storage Layer

Data is stored in a SQLite database to enable structured querying and efficient data handling.

### Tables:
- `fact_social_media` → YouTube engagement dataset  
- `fact_trends` → Google Trends dataset  
---

## 🧮 Sample SQL Query

Example query used to aggregate candidate engagement:

```sql
SELECT 
    candidate_name,
    SUM(views) AS total_views,
    SUM(engagement) AS total_engagement
FROM fact_social_media
GROUP BY candidate_name;

This layer ensures the project follows a real-world data pipeline:

**Raw Data → Cleaned Data → Stored Data → Analysis**

## 📊 Analytical Views

SQL views were created to transform raw data into analytical insights:

- vw_candidate_engagement
- vw_candidate_trends
- vw_candidate_popularity

These views serve as the foundation for downstream analysis and dashboarding.

## 📈 Popularity Model

A composite popularity score was developed using:

- Engagement Rate (YouTube)
- Search Interest (Google Trends)

This enables ranking candidates based on both attention and public interest.

---

## 📌 Next Steps

- Build Power BI data model
- Develop interactive dashboard
- Generate insights and candidate rankings