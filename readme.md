# Dynamic Price Optimization Recommendation Engine
### Sprint 0 – Planning & Setup Documentation

---

## 1. Project Overview

This project aims to build a Dynamic Price Optimization Engine that recommends optimal markdowns for low-performing retail products.  
The system analyzes sales velocity, inventory availability, competitor pricing, and demand elasticity to produce data-backed price recommendations.

The final output includes:
- Optimized markdown percentages  
- New recommended prices  
- Impact estimation (before/after KPIs)  
- A Streamlit dashboard for visualization  

---

## 2. Problem Statement Understanding

Retailers face multiple challenges:
- Products selling slower than expected  
- Excess inventory occupying working capital  
- Competitors offering lower prices  
- Lack of timely markdown strategies  

The problem requires building an automated system that:
1. Ingests product, sales, inventory, and competitor datasets  
2. Engineers features like velocity, stock health, competitiveness  
3. Applies pricing logic  
4. Outputs data-backed recommendations  

---

## 3. Finalized Solution Approach

### Core Components
1. **Data Ingestion Layer**  
   Load Kaggle datasets for products, sales, inventory, and competitor prices.  
   Standardize columns and unify them into a single master dataset.

2. **Feature Engineering Layer**  
   - Weekly sales velocity  
   - Inventory health (stock-to-demand ratio)  
   - Competitiveness score  
   - Elasticity indicator  

3. **Price Optimization Engine**  
   Rule-based strategy:
   - Identify low-performing SKUs  
   - Apply markdown percentages based on demand, stock, and competitor gap  
   - Estimate improvements  

4. **Recommendation Generator**  
   Outputs:  
   - Markdown %  
   - New price  
   - Review window (7–14 days)

5. **Dashboard Layer**  
   A Streamlit dashboard for:
   - Visual exploration  
   - SKU-level recommendations  
   - Downloadable CSV output  

---

## 4. Dataset Selection and Mapping

| Requirement | Kaggle Dataset |
|------------|----------------|
| Product catalog | Retail Product Dataset |
| Sales line items | Sample Sales Dataset |
| Inventory snapshot | Product Inventory Dataset 2025 |
| Competitor pricing | Competitor Pricing Dataset |

Additional dataset documentation will be placed inside `/data/`.

---

## 5. High-Level Architecture

```
Data Sources (Kaggle CSVs)
        |
        v
Data Ingestion & Cleaning
        |
        v
Feature Engineering Layer
        |
        v
Price Optimization Engine
        |
        v
Recommendation & Impact Module
        |
        v
Streamlit Dashboard / CSV Output
```

A visual architecture diagram will be placed under `/docs/`.

---

## 6. Project Roadmap

### Backend
- Dataset ingestion scripts  
- Data merging and cleaning  
- Feature engineering  
- Pricing engine implementation  
- KPI computation  
- Unit testing  

### Frontend (Dashboard)
- Streamlit setup  
- UI layout for filters and tables  
- Visualizations (velocity vs stock, competitor gaps)  
- CSV export  

### Deployment
- Environment setup  
- Requirements.txt  
- Optional Streamlit Cloud deployment  

---

## 7. Tech Stack

- Python 
- pandas  
- numpy  
- matplotlib / seaborn  
- scikit-learn (optional)  
- Streamlit  

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
│── README.md
│── requirements.txt
```

---
