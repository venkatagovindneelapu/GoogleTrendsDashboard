# Google Trends Dashboard

## 📌 Project Overview
This Power BI dashboard leverages **Google Trends API via SerpAPI** to track and analyze real-time and historical keyword search interest across five major sectors:

> **Jobs, Education, Finance, Technology, and Healthcare**

The project reveals what people are actively seeking across different countries—whether it's job opportunities, upskilling, financial advice, tech awareness, or health-related trends. By visualizing these patterns, the dashboard empowers stakeholders to make **informed decisions based on public search behavior**.

---

## 🧰 Technology Stack
- **SerpAPI - Google Trends API** for real-time & historical trend extraction
- **Power BI** for building visual, filterable dashboards
- **Power Query (M language)** to call APIs and process JSON
- **Python (Pandas, NumPy)** for data validation and structure testing
- **DAX (Data Analysis Expressions)** for trend calculations and KPI metrics

---

## 🔄 Data Sources & Query Design
All keyword trend data was fetched via **SerpAPI**, using the following Google Trends API calls:

### ✅ 1. Country-Wise Interest (Geo Trends)
```m
https://serpapi.com/search.json?engine=google_trends&q=Jobs,Education,Finance,Technology,Healthcare&data_type=GEO_MAP&date=today 5-y&tz=-330&api_key=YOUR_KEY
```
Returns interest by country/region over a 5-year period.

### ✅ 2. Historical Keyword Timeseries
```m
https://serpapi.com/search?engine=google_trends&q=Jobs,Education,Finance,Technology,Healthcare&data_type=TIMESERIES&date=all&tz=-330&api_key=YOUR_KEY
```
Used in Page 2 to show **keyword trends over the past 5+ years**.

### ✅ 3. Last 7 Days Real-Time Tracking
```m
https://serpapi.com/search?engine=google_trends&q=Jobs,Education,Finance,Technology,Healthcare&data_type=TIMESERIES&date=now 7-d&tz=-330&api_key=YOUR_KEY
```
Drives real-time charts (Page 3) to show **current public interest**.

### ✅ 4. Related Keywords (Rising & Top)
```m
https://serpapi.com/search.json?engine=google_trends&q=The Developer&data_type=RELATED_TOPICS&api_key=YOUR_KEY
```
Used in Page 4 to distinguish between **Rising vs. Top Keywords**.

---

## 📊 Dashboard Page Explanations

### 🌍 Page 1: **Country-Wise Keyword Insights**
- **Visuals**: World Map + Bar Chart + Line Graph + Sankey Chart
- **Metrics**:
  - Total Interest: **27K+** (Sum of keyword searches)
  - Highest: **Jobs (~15K)**
  - Lowest: **Technology (~2.7K)**
- **Insight**: Regions like Argentina showed highest interest in "Jobs," suggesting employment needs dominate.

### 🕒 Page 2: **Keyword Trends Over Time**
- **Visuals**: Line Chart by Year + Sector Filters + Pie Chart
- **Data**: 5-year historical breakdown
- **Insight**: "Education" saw consistent growth since 2020; "Finance" dipped during early 2021.
- **Filters**: Year, Quarter, Month, Sector

### 📅 Page 3: **Last 7 Days Real-Time Analysis**
- **Visuals**: Multi-colored stacked bar, donut chart, trend line
- **Timeframe**: March 12–19
- **Trending Keyword**: **Education** on March 18
- **Search Volume**: **22K**, Popularity Score: **845**

### 📈 Page 4: **Rising vs. Top Keywords (Keyword Strength)**
- **Rising Keywords**:
  - "Cover Letter" (70)
  - "Full-Time Job" (40)
- **Top Keywords**:
  - "Job" (100)
  - "Remote Work" (8)
- **Category Highlighted**: **Academic Discipline – 257.00**
- **Insight**: Indicates strong rising interest in job-seeking and education pathways

---

## 🎛 Interactive Features
- ✅ Filter by **Date, Sector, Country**
- 🔄 Pulls **latest SerpAPI data** automatically
- 📍 Navigation between pages with action buttons
- 🧠 DAX Measures used for:
  - Popularity Score
  - Total Interest
  - Real-time trending rank

---

## 🚀 Deployment Strategy
1. Paste provided M scripts in Power BI advanced editor
2. Replace `api_key` with your SerpAPI key
3. Set refresh schedule in Power BI Service (optional)

---

## 💡 Why This Project Matters
> **Search trends reveal intention.**

When a country's most searched term is "Jobs," it's not just data—it's a signal. That country’s people are actively looking for opportunities. If "Education" is trending, it suggests a desire for learning or upskilling.

This dashboard **translates public interest into actionable insight**.


---

## 🧠 Future Enhancements
- ✅ Integrate **Prophet or ARIMA** forecasting
- ✅ Add keyword-based **job recommendations**
- ✅ Predict sectoral demand by geography

---

## 👋 Let’s Connect
Want to try the dashboard or need help building trend intelligence tools? Message me or connect on [LinkedIn](#).

---

