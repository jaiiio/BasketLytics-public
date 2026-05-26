
 # BasketLytics

**End-to-end Data Engineering project** for the Argentine Professional Basketball League (LNB).

While NBA and European leagues have rich public advanced statistics, the LNB lacks accessible advanced metrics (TS%, eFG%, USG%, etc.).

### 🎯 Objective
Build a modern **Lakehouse** platform to generate advanced basketball analytics for San Lorenzo de Almagro (and eventually the entire league).

---

### 🛠 Tech Stack

- **Ingestion**: Python + Playwright (Web Scraping)
- **Storage**: Parquet + Delta Lake
- **Processing**: Spark SQL + Databricks
- **Architecture**: Medallion Architecture (Bronze → Silver → Gold) + Star Schema
- **Orchestration**: Databricks Workflows (in progress)

---

### 📊 MVP - Stage 1 (Completed)

- Scraped official data from [laliganacional.com.ar](https://laliganacional.com.ar)
- Implemented full **Medallion Architecture**:
  - **Bronze**: Raw data
  - **Silver**: Cleaned, transformed and quality-checked data
  - **Gold**: Advanced metrics ready for analysis
- Built Star Schema for analytical queries
- Performed EDA on every layer to ensure data quality
- Created initial dashboards for quick insights

**Screenshots:**

<img width="983" height="786" alt="image" src="https://github.com/user-attachments/assets/35793e72-caa8-48e3-ae9a-d922c263e6e3" />


  ### 🚀 How to Run the Project (Local / Databricks)

**Próximamente** — Working on it.

### Future Roadmap

- Stage 2: Expand to all teams in the league
- Stage 3: Comparative analysis with NBA/Europe
- Stage 4: Play-by-play data
- Stage 5: Interactive dashboards (Power BI / Streamlit / Grafana)

---

### Update 05/26/2026

## Stage 2 — Scale to all teams ✅

Expanded the pipeline from San Lorenzo to the full LNB league — 19 teams, 342 regular season games. Built 3 independent scrapers, extended the Medallion Architecture and Star Schema to cover all teams, and calculated advanced metrics league-wide including ORtg, DRtg, Net Rating, TS%, eFG% and USG%.

<img width="1487" height="862" alt="image" src="https://github.com/user-attachments/assets/7e7ea751-6f74-449b-b87b-286388932816" />



laliganacional.com.ar → Playwright → Parquet → Databricks
                                                    ↓
                                               Bronze (raw)
                                                    ↓
                                               Silver (clean)
                                                    ↓
                                               Gold (metrics)
                                                    ↓
                                              Dashboard

                                              

**Autor**: Fabio Fernández  
**Estado**: Stage 2 Completed (May 2026)
