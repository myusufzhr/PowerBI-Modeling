There are multiple data sources in this report. 
The semantic model follows a **Star Schema**. 

**Fact Tables** - 

1. **FactInternational_Credit_Portfolio** -
    -Storage - DirectQuery 
    -Source - Enterprise Data Lake
    -Connection Type - ODBC
    -SQL Query - check the import page. 
    -> This table contains the portfolio information such as account number (masked), outstanding balance, charge off indicator, origination score etc. for all countries. The SQL queries uses a filter in the query. 
    -> Due to size of source and the need to fetch latest data to monitor portfolio trends, the storage of this table is set to DirectQuery. 
    -> Since the data goes extensive engineering, the outstanding balance and count of accounts needs to be reconciled with the FactLocal_Chile_Portfolio

2. **FactLocal_Chile_Portfolio** - 
    -Storage - import
    -Source - CSV file uploaded to sharepoint
    -Connection type - sharepoint
    -> This table contains the extract of the local Chile database containing account numbers (unmasked), outstanding balance etc.
    -> The outstanding balance in this report is treated as accurate. 

**Dimension Tables** -

1. **Organizational hierarchy** -
    -Storage - Dual
    -Source - Enterprise Data Lake
    -Connection Type - ODBC
    -SQL Query - check the import pages

2. **Product heirarchy** - 
    -Storage - Dual
    -Source - Enterprise Data Lake
    -Connection type - ODBC
    -SQL Query - check the import pages

3. **Dates** - 
    -Storage - Dual
    -Source - Created table and measures
    -Measures - check the import pages


