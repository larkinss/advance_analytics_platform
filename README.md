# advance_analytics_platform

Databricks analytics platform deployed with Declarative Automation Bundles and GitHub Actions (dev → prod).

## What it deploys
- **Pipeline**: `sales_pipeline` (bronze → silver → gold `daily_revenue`)
- **Jobs**: `daily_etl` (daily), `train_customer_value` (weekly)
- **ML**: `customer_value_model` in Unity Catalog and a serving endpoint
- **Dashboard**: Daily revenue
- **App**: `revenue-app` (Streamlit)

## CI/CD
- **Pull request**: lint, tests, `bundle validate`
- **Merge to main**: deploy to **dev**, then deploy to **prod** after approval

