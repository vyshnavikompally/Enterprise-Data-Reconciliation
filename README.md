# Enterprise Data Architecture & Reconciliation

## Project Overview
This capstone project demonstrates an enterprise data reconciliation workflow using SQL and Python. It integrates user records, server transaction logs, and daily currency exchange rates to calculate reconciled revenue in USD and present key financial insights through a CFO dashboard.

## Objectives
- Extract the latest user status records using SQL.
- Parse and extract transaction information from server logs using Python and regular expressions.
- Handle missing daily exchange rates.
- Reconcile transactions with exchange rates and active user records.
- Convert transaction values from EUR to USD.
- Generate monthly revenue summaries and identify top customers.

## Tools and Technologies
- **Python** — data processing and reconciliation
- **SQL / SQLite** — database queries and user status extraction
- **Jupyter Notebook** — development and analysis
- **Pandas** — data cleaning, transformation, and joining
- **Regular Expressions (Regex)** — server log parsing
- **Matplotlib** — data visualization
- **GitHub** — project version control and documentation

## Project Workflow

### Phase 1: User Data Extraction
Used SQL window functions, including `ROW_NUMBER()`, to identify the latest status for each user. The latest records were filtered to identify active users.

### Phase 2: Server Log Processing
Processed server logs using Python and regular expressions to extract transaction dates, user IDs, product IDs, and EUR transaction values. Error records were excluded from the extracted transaction dataset.

### Phase 3: Data Reconciliation
Loaded daily EUR-to-USD exchange rates, handled missing rates using forward-filling where appropriate, and joined transaction records with exchange rates and active user records. Calculated reconciled revenue in USD.

### Phase 4: CFO Dashboard
Created monthly revenue summaries and a top-five-customer revenue visualization to support financial reporting and business analysis.

## Results

| Metric | Result |
|---|---:|
| Active users identified | 14,183 |
| Extracted transactions | 94,902 |
| Reconciled transactions | 53,899 |
| Monthly revenue records | 12 |
| Top customers displayed | 5 |
| Missing exchange rates after processing | 0 |
| Missing USD revenue values | 0 |

**Note:** The extracted and reconciled transaction counts differ because records were filtered during reconciliation. The exact reasons should be confirmed from the notebook's join and filtering logic.

## Project Files
- `Student_work_file (1) (1).ipynb` — Jupyter Notebook containing the project workflow and analysis.
- `daily_exchange_rates (1) (1).csv` — daily EUR-to-USD exchange rates.
- `enterprise_database (1) (1).db` — SQLite database used for user data extraction.
- `server_logs (1) (1).txt` — server log input data.
- `CFO_Dashboard.png` — generated revenue dashboard.
- `Enterprise_Data_Reconciliation_pdf.pdf` — project report.

## How to Run
1. Download or clone this repository.
2. Install the required Python packages:
   ```bash
   pip install pandas matplotlib jupyter
   ```
3. Open the notebook in Jupyter Notebook or JupyterLab.
4. Ensure the input CSV, database, and log files are available at the paths expected by the notebook.
5. Run the notebook cells in order.

## Conclusion
This project demonstrates an end-to-end data reconciliation process combining database querying, log parsing, currency conversion, data integration, and financial visualization. The resulting dashboard provides a summarized view of monthly revenue and top customers.

---
**Project:** Enterprise Data Architecture & Reconciliation  
**Type:** Capstone Project
