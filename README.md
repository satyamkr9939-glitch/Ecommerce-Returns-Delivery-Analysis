# E-commerce Returns & Delivery Analysis (1M+ Records)

## Overview
Analysis of 1,000,000 e-commerce transaction records to identify which factors — if any — are associated with order returns and delivery delays. The goal was to test common assumptions (does category, location, or seller quality drive returns?) against actual data rather than intuition.

## Dataset
- **Size:** 1,000,000 rows, 20 columns
- **Fields:** user/product/seller IDs, category, brand, price, discount, final price, rating, review count, stock, seller rating, purchase date, shipping time, location, device, payment method, return status, delivery status

## Tools Used
- Python (pandas) — data cleaning, profiling, and analysis
- Jupyter Notebook

## Process
1. **Data Profiling** — checked shape, data types, nulls, and value ranges before any cleaning
2. **Data Cleaning** — converted `purchase_date` from text to datetime; verified numeric fields (price, discount, ratings) for logical consistency
3. **Data Quality Check** — confirmed brand and category fields are independently randomized (every brand appears across all 5 categories), consistent with synthetic data generation
4. **Business Question Analysis** — tested 5 hypotheses about what drives returns and delays using group comparisons

## Key Findings

| Variable | Effect on Returns/Delays? |
|---|---|
| Category | No — return rates flat at 11.3%–11.8% across all categories |
| Location | No — delay rates flat at 29.2%–29.8% across all 5 cities |
| Seller Rating | No — nearly identical (3.75 vs 3.75) for returned vs. non-returned orders |
| Payment Method | No — return rates flat at 11.5%–11.7% across all methods |
| **Shipping Time** | **Yes** — returned orders had ~9% longer average shipping time (3.41 vs 3.13 days) |

## Business Takeaway
Across five variables tested, only **shipping time** showed a meaningful relationship with returns. Product category, seller quality, customer location, and payment method showed no measurable effect. This suggests that improving delivery speed and reliability may reduce returns more effectively than seller vetting or category-specific interventions.

## Notebook
See [`Ecommerce_analysis.ipynb`](./ecommerce_analysis.ipynb) for full code, outputs, and step-by-step markdown commentary.

## Author
**Satyam** | [LinkedIn](https://linkedin.com/in/satyam-8b105032b) | [Portfolio](https://datavedh.in)
