# Dynamic Price Optimization Recommendation Engine
### Hackathon Project – Sprint 0 (Planning & Setup)

---

## 1. Project Overview

This project aims to build a **Dynamic Price Optimization Engine** that identifies slow-moving retail products and recommends optimal markdowns.  
The system analyzes:

- Sales velocity  
- Inventory availability  
- Competitor pricing  
- Demand elasticity indicators  

The final output includes data-driven markdown percentages, new recommended prices, expected impact, and a dashboard for interactive exploration.

---

## 2. System Flowchart (Mermaid)

```mermaid
flowchart TD

    A[Data Sources<br>(Kaggle Datasets)] --> B[Data Ingestion & Cleaning<br>pandas-based ETL]

    B --> C[Feature Engineering Layer<br>Velocity, Stock-Demand Ratio,<br>Competitiveness, Elasticity]

    C --> D[Price Optimization Engine<br>Rule-Based Markdown Logic]

    D --> E[Recommendation Generator<br>Markdown %, New Price,<br>Review Window]

    E --> F[Impact Evaluation Module<br>Before/After KPI Estimation]

    F --> G[Dashboard Layer<br>Streamlit UI & Visualizations]

    G --> H[Final Output<br>CSV Export / Interactive Insights]
```

---

## 3. Problem Statement Understanding

Retailers often suffer from:
- Products selling slower than expected  
- Excess inventory tied up in non-moving SKUs  
- Competitors pricing similar products lower  
- Delayed or non-optimized markdown decisions  

This system solves these challenges by leveraging data from sales, stock levels, and competitor prices to automate markdown recommendations and drive better inventory health.

---

## 4. Finalized Solution Approach

### 4.1 Core Pipeline
1. **Data Ingestion Layer**  
   - Load product, sales, inventory, and competitor datasets from Kaggle  
   - Standardize columns  
   - Clean missing or invalid values  
   - Merge into a unified master dataset  

2. **Feature Engineering Layer**  
   - Weekly sales velocity  
   - Stock-to-demand ratio  
   - Competitiveness score  
   - Elasticity approximation  
   - Additional retail metrics as needed  

3. **Price Optimization Engine**  
   - Identify low-performing SKUs based on velocity + stock signals  
   - Apply rule-based markdown percentages  
   - Recommended markdown window (7–14 days)  
   - Estimate impact on velocity and stock depletion  

4. **Recommendation Generator**  
   - Consolidated price recommendation table  
   - New price calculations  
   - Reason codes for markdown (e.g., “High stock”, “Low demand”, “Competitor undercut”)  

5. **Dashboard Layer**  
   - Built using Streamlit  
   - Product-level insights  
   - Interactive charts (velocity vs stock, competitor gaps)  
   - CSV export  

---

## 5. Dataset Selection & Mapping (Kaggle)

| Requirement              | Kaggle Dataset                         |
|--------------------------|-----------------------------------------|
| Product catalog          | Retail Product Dataset                  |
| Sales line items         | Sample Sales Dataset                    |
| Inventory snapshot       | Product Inventory Dataset 2025          |
| Competitor pricing       | Competitor Pricing Dataset              |

These datasets simulate a realistic retail environment.

---

## 6. Project Roadmap (Sprint-Level Breakdown)

### Backend Tasks
- Setting up the project structure  
- Loading datasets via ingestion scripts  
- Creating the unified master dataset  
- Feature engineering implementation  
- Developing rule-based pricing engine  
- KPI computation (before & after)  
- Testing data transformations  

### Frontend Tasks
- Streamlit dashboard setup  
- Filters for category, product, price range  
- Product recommendation table  
- Visualizations for inventory health and competitor gaps  
- Export button for CSV  

### Deployment Tasks
- Creating requirements.txt  
- Documentation updates  
- Optional deployment on Streamlit Cloud  

---

## 7. Tech Stack

**Languages:**  
Python 3.x  

**Libraries:**  
pandas, numpy, matplotlib, seaborn, scikit-learn (optional), streamlit  

**Tools:**  
GitHub, Kaggle, Jupyter Notebook, Streamlit Cloud  

---

## 8. Repository Structure

```
/
│── backend/
│     ├── ingestion/
│     ├── feature_engineering/
│     ├── pricing_engine/
│     ├── utils/
│
│── dashboard/
│     ├── app.py
│
│── data/
│     ├── raw/
│     ├── processed/
│
│── docs/
│     ├── architecture.png
│     ├── sprint0_readme.pdf
│
│── notebooks/
│     ├── main_pipeline.ipynb
│
│── requirements.txt
│── README.md
```

---

## 9. Sprint 0 Deliverables

- Understanding of the problem statement documented  
- Kaggle datasets selected and mapped  
- End-to-end architecture finalized (Mermaid + diagrams)  
- Solution approach defined  
- Tech stack confirmed  
- Repository structure created  
- README populated with Sprint 0 outcomes  

---

## 10. Next Steps (Sprint 1)

- Begin implementing ingestion and feature engineering  
- Create master dataset  
- Build the initial pricing engine logic  
- Prepare baseline dashboard structure  
