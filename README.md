# Car Sales and Profit Analysis by Dealer

An Excel and Power BI analysis of five years of car dealership transactions (2021–2025). The project answers a simple management question: **which dealers sell the most cars, which earn the most profit, and how has that changed year on year?** Raw sales records were modelled into pivot tables and an Excel dashboard, and then rebuilt as an interactive Power BI report with year and model slicers.

## Dataset

The `Raw Data` sheet in `CarSalesByModelEnd.xlsx` holds **3,000 transaction rows** with these fields:

| Field | Description |
|---|---|
| Year, Month, Date | Date of sale (2021–2025) |
| Model | One of five models: Beaufort, Champlain, Hudson, Labrador, Salish |
| Dealer ID | One of 10 dealers (1212, 1215, 1217, 1222, 1224, 1288, 1301, 1336, 1401, 1402) |
| Quantity Sold | Units sold in the transaction |
| Profit | Profit earned on the transaction |

## Approach

1. **Data preparation (Excel):** added a text date key (`Date 1`) to the raw data so it can be used as a pivot row field.
2. **Pivot analysis (Excel):**
   - Profit by Year and Dealer ID
   - Profit by Date and Model
   - Quantity Sold by Dealer ID
   - Profit by Dealer for a single model (Hudson)
3. **Excel dashboard:** a `Dashboard` sheet with a headline Total Profit figure and charts built on the pivots.
4. **Power BI report (`Cars Sales Analysis.pbix`):** one report page with:
   - Gauges for total profit and total quantity sold
   - Line chart of quantity sold by dealer
   - Pie chart of quantity sold by model
   - Ribbon chart of profit and quantity by dealer and model
   - Waterfall chart of profit contribution by dealer
   - Slicers for Year and Model

## Key Findings

These figures come from the pivot tables in the workbook:

- **Total profit:** 78,402,279 across all dealers, models and years.
- **Total units sold:** 58,118.
- **Highest-volume dealer:** Dealer **1288**, with 7,119 units. It also has the highest profit in every year from 2021 to 2025 (peak of 2,058,232 in 2023).
- **Lowest-volume dealers:** Dealer **1222** (4,536 units) and Dealer **1402** (4,673 units). They also have the lowest annual profit.
- **Trend:** profit rose from 2021 to 2023 for every dealer, then fell in 2024 and again in 2025.
- **Hudson model:** Dealer 1288 earns the most Hudson profit (1,406,258) and Dealer 1222 the least (878,586).

## Tools & Tech

- **Microsoft Excel:** pivot tables, pivot charts, dashboard sheet
- **Power BI Desktop:** data model, interactive visuals, slicers

## Repository Structure

```
.
├── CarSalesByModelEnd.xlsx     # Raw data, pivot tables and Excel dashboard
├── Cars Sales Analysis.pbix    # Interactive Power BI report
├── LICENSE
└── README.md
```

Workbook sheets: `Dashboard`, `Profit by Date Vs Model`, `Profit by Year & Dealer ID`, `Sum of Profit by Hudson Model`, `Qty Sold by Dealer Id`, `Raw Data`.

## How to Open

1. Clone or download the repository.
2. Open `CarSalesByModelEnd.xlsx` in Microsoft Excel to see the raw data, the pivots and the dashboard.
3. Open `Cars Sales Analysis.pbix` in [Power BI Desktop](https://powerbi.microsoft.com/desktop/), which is free on Windows. Use the Year and Model slicers to filter the visuals.

## License

Released under the [MIT License](LICENSE).

---

**Author:** Anshuman Tewary · [GitHub](https://github.com/anshumantewary-pm) · [LinkedIn](https://www.linkedin.com/in/tewary-anshuman/)
