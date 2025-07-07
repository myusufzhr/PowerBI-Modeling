# Retail Credit Portfolio Reconciliation & Monitoring (Power BI Report)

This Power BI report extracts data from Hive (Enterprise Data Lake) and integrates it with external files shared by local teams. It performs transformations within Power BI to support analytical and reporting needs.

## 📌 Purpose
- Reconcile data between the Enterprise Data Lake and manually shared text file.
- Ensure data quality for use in the Enterprise Stress Model.
- Monitor performance across retail credit portfolios such as mortgages, credit cards, and personal loans.

## 🛠️ Technologies Used
- Power BI (Data model, DAX, and paginated report)
- Hive (Enterprise Data Lake)
- ODBC connection
- SQL (for queries against the lake)

## 🔗 Data Sources
For details on fact and dimension tables, data types, and query methods, refer to the [Source Information](./Source).
