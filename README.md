\# 🏀 NBA Player Value Analytics Dashboard    
\*\*An end-to-end player valuation and trade insights project using Python, Excel, and Tableau\*\*

\#\#\# \> 🎯 View the interactive Tableau dashboard here:    
\> \[🔗 Tableau Public Link\](\#) \*(Replace with your actual URL)\*

\---

\#\# 📊 Project Overview

This project focuses on evaluating NBA player value by comparing player performance metrics with salary data to inform trade decisions and roster optimization. It simulates the work of a front office analyst by integrating real-world scraping, advanced data modeling, clustering, and an executive-ready interactive Tableau dashboard.

\---

\#\# 🧰 Tools & Technologies Used

| Tool           | Purpose                                      |  
|----------------|----------------------------------------------|  
| \*\*Python (pandas, BeautifulSoup)\*\* | Web scraping, cleaning, feature engineering |  
| \*\*Scikit-learn\*\* | KMeans clustering for player segmentation  |  
| \*\*Plotly Express\*\* | Interactive EDA & exploratory charts     |  
| \*\*Excel\*\*      | Final cleaning, manual deduplication, team adjustments |  
| \*\*Tableau\*\*    | Interactive executive dashboard              |  
| \*\*Task Scheduler\*\* | Automation pipeline for data refresh     |

\---

\#\# 🎯 Business Objectives

\- Identify undervalued and overvalued NBA players based on performance and salary  
\- Evaluate player contributions using custom metrics beyond traditional stats  
\- Cluster players into actionable groups (e.g. high-value targets, overpaid contracts)  
\- Support GM decisions on trade targets, salary cap management, and scouting

\---

\#\# 🔍 Methodology

\#\#\# 🗂 Phase 1: Data Collection (Python)  
\- Scraped salary tables using \`requests\` \+ \`BeautifulSoup\`  
\- Loaded player stats using \`pandas.read\_html\`  
\- Merged salary and stats tables on player and team  
\- Handled edge cases (Non-standard encodings)

\#\#\# 🧼 Phase 2: Data Cleaning & Integration  
\- Flattened multi-indexed salary tables  
\- Standardized team abbreviations and removed corrupted names  
\- Converted salary to numeric values  
\- Exported cleaned data to Excel (\`nba\_collecting\_output.xlsx\`) for final deduplication  
\- Manually removed traded duplicates (e.g., PJ Tucker), resolved \`team\_x/team\_y\`, dropped awards  
\- Final result: \`nba\_cleaned.xlsx\`

\#\#\# 🧪 Phase 3: Feature Engineering & Clustering  
\- Imported cleaned data into Python (\`nba\_cleaned.xlsx\`) for Data Analysis  
\- Built custom metrics:  
  \- \*\*Efficiency Score\*\*: \`(PTS \+ REB \+ AST \- TOV) / GP\`  
  \- \*\*Efficiency per Million\*\*: Efficiency scaled by salary  
  \- Flags for \`Undervalued\` / \`Overvalued\` players (based on medians)  
\- Clustering:  
  \- Used \`KMeans\` on scaled features: efficiency, usage %, salary  
  \- Created \`value\_cluster\` column to group players into 4 strategic buckets  
\- Final result: \`nba\_final.xlsx\`

\#\#\# 📈 Phase 4: Visualization in Tableau  
Created an executive dashboard aligned with GM decision-making needs:  
\- 📊 \*\*Efficiency vs Salary Quadrant\*\* – See tradeoffs between cost and contribution  
\- 🎯 \*\*Top Undervalued Players Table\*\* – Filterable player shortlists  
\- 🔥 \*\*Team Needs Heatmap\*\* – Identify trade partners based on team structure  
\- 📍 Filters by position, team, role, and value cluster

\#\#\# ⚙️ Phase 5: Automation  
\- Final Python script outputs dashboard-ready \`.csv\`  
\- Scheduled with Windows Task Scheduler  
\- Tableau auto-refreshes data source on open or schedule

\---

\#\# 💡 Key Insights & Recommendations

\#\#\# 🔎 Insights  
\- \*\*Tyus Jones\*\* and \*\*Scottie Barnes\*\* identified as top value trade targets based on salary-efficiency imbalance  
\- Teams like \*\*Phoenix\*\* are strong sell candidates (high efficiency, high salary)  
\- \*\*CHI/DET\*\* are good offloading targets for cap relief

\#\#\# 🧠 Strategic GM Recommendations  
\- Retain/acquire top value players based on cluster & flag metrics  
\- Rebalance rosters by trading overpaid underperformers  
\- Target teams with high team efficiency and bloated salary caps  
\- Monitor undervalued player list weekly using auto-refreshed dashboard

\---

`## 📘 Lessons Learned`

`- Improved efficiency in cleaning complex multi-index datasets`  
`- Navigated real-world web scraping obstacles (HTML comments, encoding issues)`  
`- Strengthened clustering skills and business-focused feature engineering`  
`- Designed end-to-end analytics projects from raw scrape to executive dashboard`

\---

\#\# 📂 Dataset Overview

\- Player stats (basic & advanced): \[Basketball-Reference\](https://www.basketball-reference.com)  
\- Contract data (salaries): \[Basketball-Reference Contracts\]([https://www.basketball-reference.com/contracts/players.html](https://www.basketball-reference.com/contracts/players.html))

`---`

`## 📄 Supporting Materials (in order of use)`

``- ✅ `nba_collecting.ipynb`: Python script for web scraping, salary/stats extraction, and basic cleaning to allow merging``  
``- ✅ `salaries_raw.csv`: Raw salary data scraped from Basketball Reference``  
``- ✅ `stats_raw.csv`: Raw player stats data (basic and advanced) from Basketball Reference``  
``- ✅ `cleaning_step1.ipynb`: Python script of initial cleaning and merging of raw stats/salaries into 1 dataset``  
``- ✅ `dataset_partial_cleaned.xlsx`: Merged and partially cleaned dataset exported from Python for Excel-based final cleanup``  
``- ✅ `dataset_fully_cleaned.xlsx`: Cleaned dataset with duplicates removed, team names standardized, and manual corrections applied``  
``- ✅ `nba_analysis.ipynb`: Python script for feature engineering, clustering,data analysis, and exporting dashboard-ready CSV``  
``- ✅ `dataset_final.xlsx`: Final cleaned dataset with additional calculated metrics used for Tableau dashboard and decision-making analysis``  
``- ✅ `nba_dashboard.twbx`: Interactive Tableau dashboard file containing all roughwork/visuals/filters and final dashboard for presentation``  
``- ✅ `README.md`: Full project documentation, methodology, business insights, and dashboard link``
