# Manufacturing Operations Analytics BI Dashboard

Interactive **Power BI** manufacturing operations analytics solution built over a **9-table, 31,991-row Star Schema** tracking production runs, machine utilization, employee output, scrap/rejection efficiency, and buyer/customer fulfillment.

---

## Overview

Manufacturing floor supervisors and plant managers need synchronized KPI visibility across production batches, equipment capacity, operator accountability, and rejection rates. This repository packages the Power BI workbook (`Manufacturing.pbix`), the 9-table normalized Star Schema source workbook (`data/Manufacturing Project Data.xlsx`), and the KPI & column dictionary documentation (`docs/`).

---

## Key Features

- **Production Output vs. Rejections:** Tracks manufactured vs. rejected units across operations, machines, and departments.
- **Machine & Operation Efficiency:** Evaluates machine-level throughput across `86` machines and `10` distinct manufacturing operations.
- **Workforce & Customer Allocation:** Links `10,679` production transactions to `899` employees, `9,944` customers, and `10,000` catalog items.
- **Schema & KPI Documentation:** Includes column definitions (`docs/COLUMN DISCRIPTION OF MANUFECTURING DATA.docx`) and KPI matrix (`docs/KPI Metrics list.xlsx`).

---

## Data Model (`9-Table Star Schema` · `31,991` Data Rows)

| Worksheet / Table | Type | Data Rows | Purpose |
| :--- | :--- | :---: | :--- |
| `fact_Production` | Fact | `10,679` | Transaction-level manufacturing orders, quantities, and rejection metrics |
| `dim_Item` | Dimension | `10,000` | Product/SKU master attributes |
| `dim_Customer` | Dimension | `9,944` | Customer lookup records |
| `dim_Employee` | Dimension | `899` | Operator / employee master |
| `dim_Date` | Dimension | `365` | Annual calendar dimension |
| `dim_Machine` | Dimension | `86` | Machine and equipment assets |
| `dim_Operation` | Dimension | `10` | Shop-floor manufacturing stages |
| `dim_Buyer` | Dimension | `4` | Institutional buyer segments |
| `dim_Department` | Dimension | `4` | Functional plant departments |

*(Plus `⭐ Schema Guide` worksheet inside [`Manufacturing Project Data.xlsx`](data/Manufacturing%20Project%20Data.xlsx).)*

---

## Technology Stack

- **Business Intelligence:** Power BI Desktop, DAX, Power Query
- **Data Store & Documentation:** Microsoft Excel (`.xlsx`), Word (`.docx`)

---

## Project Structure

```text
Manufacturing-Operations-BI/
├── data/
│   └── Manufacturing Project Data.xlsx                  # 9-table Star Schema dataset
├── docs/
│   ├── COLUMN DISCRIPTION OF MANUFECTURING DATA.docx    # Field dictionary
│   ├── KPI List And Detail.txt                          # KPI reference link
│   └── KPI Metrics list.xlsx                            # KPI calculation definitions
├── Manufacturing.pbix                                   # Interactive Power BI report
├── LICENSE                                              # MIT License
└── README.md
```

---

## How to Open

1. Download [`Manufacturing.pbix`](Manufacturing.pbix).
2. Open in **Power BI Desktop**.
3. If refreshing data sources locally, repoint Power Query to [`data/Manufacturing Project Data.xlsx`](data/Manufacturing%20Project%20Data.xlsx).

---

## License

MIT License — see [LICENSE](LICENSE).

## Author

**Yogesh Patil** — [@yogesh-patil2003](https://github.com/yogesh-patil2003) · [LinkedIn](https://www.linkedin.com/in/yogeshpatil2003/) · [Email](mailto:officialyogeshpatil0@gmail.com)
