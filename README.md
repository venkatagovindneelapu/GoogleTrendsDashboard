# Google Trends Dashboard

## 📅 Project Overview

This project is a **real-time keyword trend analysis dashboard** powered by the **Google Trends API**, focused on five critical sectors: **Jobs, Education, Finance, Technology, and Healthcare**. The core idea is that **what people search most reflects what they want or need most**. Whether it's skill gaps, job demand, or rising public interest, this dashboard helps decode user intent across countries.

The dashboard empowers:
- 📈 **Businesses** to align strategies with rising market demand
- 🎓 **Educators** to understand trending skills
- 📄 **Governments** to identify regional needs
- 🚀 **Job seekers** to focus on in-demand areas

---

## 🛠️ Technology Stack
- **Google Trends API** – Fetching real-time keyword data
- **Python (Pandas, NumPy, Requests)** – Cleaning and processing
- **SQL (PostgreSQL)** – Data storage and query optimization
- **Power BI** – Visual storytelling and dashboarding
- **DAX** – Custom measures and insights

---

## 📦 Data Flow Architecture

1. **Data Extraction**: Google Trends API is queried for search volume data by sector and country.
2. **Data Processing**: Python scripts clean, transform, and structure the data.
3. **Storage**: Processed data is pushed into SQL tables.
4. **Visualization**: Power BI fetches from SQL, computes insights via DAX, and presents the findings.

---

## 📈 Dashboard Pages & Visual Insights

### 🌐 Page 1: Country-Wise Keyword Trends ("Overview")
- **Objective**: Identify which sector is most searched in a selected country.
- **Visuals**: Sankey diagram, Pie chart, and Line chart.
- ✅ **Insight**: Argentina, for example, shows "Jobs" as the top search sector, indicating workforce demand and employment intent.
- **Card**: Total Search Interest = **22K**; Interest Share = **20%**.

### 🗒️ Page 2: Keyword Performance by Date
- **Objective**: Track sector keyword activity across a timeline.
- **Visuals**: Stacked bar chart and donut chart over **March 12–19**.
- ✅ **Insight**: March 18 showed a spike in "Jobs" and "Education" interest, showing short-term needs, likely exam or job deadline-related.
- **Highlights**: Trending Keyword = **Education**, Search Volume = **22K**, Popularity Score = **845**.

### ⏱️ Page 3: Last 7 Days Real-Time Analysis
- **Objective**: Live trend monitoring based on the latest weekly data.
- **Visuals**: Date-filtered bar charts and a global keyword map.
- ✅ **Insight**: Visualizes how keyword activity changes **daily**, showing spikes and drops in interest per country.

### 🌟 Page 4: Rising vs. Top Keywords
- **Objective**: Distinguish between fast-growing and consistently top keywords.
- **Visuals**: Bar + line chart, KPI tiles.
- ✅ **Insight**:
  - **Rising**: "Cover Letter" (70), "Full-time Job" (40)
  - **Top**: "Job" (100), "Remote Work" (8), "Part-time Job" (5)
- **Category Card**: "Academic Discipline" appears with a popularity score of **257**, suggesting intense interest in educational advancement.

---

## 🔄 Interactive Features
- ✉ **Filter by Country, Sector, Date**
- ⏰ **Real-time Updates from Google Trends API**
- 👌 **Smooth navigation buttons between pages**

---

## 🚄 Deployment & Maintenance

### Deployment Steps
1. API setup with `pytrends`
2. Data extraction and processing in Python
3. Storage into SQL
4. Power BI data connection and report building
5. Publish via Power BI Service

### Maintenance Strategy
- ⏳ Automate daily fetch/update scripts
- ⚡ Optimize SQL queries for performance
- 🌐 Expand industry filters & country scope

---

## 📅 Why I Built This
The idea behind this project is simple yet impactful: **People's search intent is a reflection of their needs**.

If "Jobs" are the most searched sector in a country, then people there are **seeking employment** or career change. If "Education" spikes, they may be **trying to upskill**. This dashboard brings those patterns to light.

It bridges the gap between **search data and strategic action**, helping users understand where interest lies and **how to act on it**.

---

## 💼 Use Cases & Benefits
- 💼 **Recruiters**: Identify hiring trends and popular job terms.
- 🌐 **Governments**: Detect economic shifts and societal needs.
- 📚 **Educators**: Tailor course offerings to trending skills.
- 🚀 **Marketers**: Time campaigns around what people are actively searching.

---

## 🎉 Final Thoughts
This dashboard turns **Google Search data into decision-making gold**. As it evolves, I plan to add:
- Forecasting via **Prophet/ARIMA**
- Cross-country comparisons
- Skill-gap mapping

Thanks for reading! Feel free to ⭐ this repo or connect with me on [LinkedIn](#) if you'd like to collaborate on more data-driven projects!

---

