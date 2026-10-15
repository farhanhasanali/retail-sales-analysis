# Retail Sales Analysis | PostgreSQL

## Project Overview

This project analyzes 2024 retail sales transactions using PostgreSQL to evaluate revenue, compare Online and Physical Store channels, examine discount patterns, and rank products.

## Business Questions

- What was the annual revenue and order volume?
- How did Online and Physical Store contribute to revenue?
- How did revenue change month over month and by quarter?
- How did discounts compare across channels?
- Which products generated the most revenue?

## Tools and Skills

- PostgreSQL and SQL
- Aggregate functions and date functions
- Common Table Expressions (CTEs)
- Window functions, including LAG, DENSE_RANK, and SUM OVER
- Data quality checks and business analysis

## Repository Structure

```text
retail-sales-analysis/
├── retail_sales_analysis.sql
└── README.md
```

## Key Findings

- Online generated 51.55% of annual revenue; Physical Store contributed 48.45%.
- Online led revenue during the first three quarters, while Physical Store outperformed Online in Q4.
- Laptops and Smartphones collectively represented approximately 47.6% of annual revenue.
- Discount rates were similar across the two channels.

## Dataset and Assumptions


| Column | Purpose |
|---|---|
| `transaction_id` | Transaction or order identifier |
| `transaction_date` | Transaction date |
| `sales_channel` | Online or Physical Store |
| `product_name` | Product name |
| `quantity` | Units sold |
| `unit_price` | Price per unit before discount |
| `discount_pct` | Discount as a decimal, e.g. 0.10 for 10% |

Revenue is calculated as quantity × unit price × (1 − discount rate).
## How to Run

1. Install PostgreSQL and open pgAdmin or another SQL client.
2. Load your dataset into a table named `retail_sales`.
3. Confirm that the columns and data types match the assumptions above.
4. Open `retail_sales_analysis.sql` and execute the queries.
5. Compare the output with the reported findings and update this README as needed.

## Limitations

- **Profitability:** Product costs and operating expenses were unavailable, so profit and profit margin could not be calculated.
- **Discount impact:** Observed relationships do not establish that discounts caused changes in sales.
- **Seasonality:** One year of data cannot confirm recurring annual seasonal patterns.
- **Customer behavior:** Sales transactions alone do not establish customer preferences or satisfaction.

## Conclusion

This project demonstrates how PostgreSQL can transform transactional retail data into business insights through channel comparisons, monthly and quarterly trends, discount analysis, and product rankings. Further work with multiple years of data, product costs, and customer-level information could deepen the analysis.

## Author

Farhan B Hasanali

**Project category:** Data Analytics | SQL | Retail Sales
