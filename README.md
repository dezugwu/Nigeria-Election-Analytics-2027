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

## 📊 Data Sources (Phase 1)
- YouTube (video engagement data)
- Google Trends (search interest)

---

## ⚙️ Tools & Technologies
- Python (data extraction & processing)
- Power BI (data visualization)
- APIs (YouTube Data API)
- Pytrends (Google Trends)

---

## 🧱 Project Status
🚧 In Progress (Day 3 — Data Collection (YouTube))

---

## 🧱 Data Architecture (Current Design)

The project follows a structured data modeling approach:

### Fact Table
- Social media activity (views, likes, comments, engagement)

### Dimension Tables
- Candidates
- Date
- Platform

This structure ensures scalability and supports advanced analytics such as trend analysis, growth tracking, and candidate comparison.

---

## 📊 Data Collection (Phase 1)

Initial dataset has been extracted using the YouTube Data API.

The dataset includes:
- Video titles
- Views, likes, and comments
- Published date
- Candidate association

This forms the first layer of the analytics pipeline.

## 📌 Next Steps
- Data extraction using YouTube API
- Google Trends integration
- Initial dataset creat