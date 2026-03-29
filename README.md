# Healthcare Procurement Spend Analytics
### SYST52461 — Big Data Storage and Analysis | Term Project

A big data pipeline built on Databricks and PySpark that simulates a regional hospital network's procurement system. The pipeline processes vendor, purchase order, and spend data through the medallion architecture (Bronze → Silver → Gold) and delivers insights through a live dashboard.

---

## Scenario

A regional hospital network wants visibility into its procurement spend, who they are buying from, what they are buying, and where costs are concentrated. This pipeline identifies top vendors by spend, tracks monthly trends, classifies spend by category, and flags late payments against vendor payment terms.

---

## Notebooks

| Notebook | Description |
|---|---|
| `01_bronze_ingestion.ipynb` | Generates mock data and writes Bronze Delta tables |
| `02_silver_processing.ipynb` | Cleans Bronze tables and writes Silver Delta tables |
| `03_gold_aggregation.ipynb` | Joins and aggregates Silver into Gold tables |
| `04_eda_analysis.ipynb` | EDA, KPI summary, and dashboard visualizations |

Run notebooks in order. Each notebook depends on the previous one completing successfully.

---

## Setup

1. Import all notebooks into your Databricks workspace
2. Attach to a cluster running **Databricks Runtime 11.3 LTS or above**
3. Run `01_bronze_ingestion.py` first — this creates the catalog and schema
4. Run remaining notebooks in sequence

**Catalog:** `healthcare_procurement`  
**Schema:** `procurement_analytics`
