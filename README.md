# Sales Intelligence

A Power BI retail sales project using the Superstore dataset, with sales, profit, order count, and profit margin measures; monthly trends; category, regional, and customer-segment comparisons; and year and region slicers.

## Files

- `data/Sample - Superstore.csv`: source data.
- `powerbi/Sales Intelligence.pbix`: report, model, and imported data; open in Power BI Desktop.

The PBIX contains the report and model. Keep the source CSV for refresh.

## Open and refresh

1. Clone this repository or download and extract its ZIP.
2. Open `powerbi/Sales Intelligence.pbix` in Power BI Desktop.
3. Select **Transform data**, select the **Superstore** query, and open **Advanced Editor**.
4. Set `CsvPath` to the full path of `data/Sample - Superstore.csv` on your computer. The current value is `D:\POWER BI\Sales-Intelligence\data\Sample - Superstore.csv`.
5. Select **Done**, then **Close & Apply**, and refresh.

The PBIX includes imported data. Update the CSV path before refreshing on another computer. Use Power BI Desktop to interact with the report.

The report has a saved Year selection of **2015**. Clear the year and region slicers to view the full dataset. The **Overall dataset insights** text box contains static text and does not recalculate with slicer selections.

## Measures

| Measure | Calculation |
| --- | --- |
| Total Sales | Sum of Sales |
| Total Profit | Sum of Profit |
| Total Orders | Distinct count of Order ID |
| Profit Margin | Total Profit / Total Sales, returning 0 for a zero denominator |

Power Query applies column types using the en-US locale and derives Year and Month Start from Order Date. The CSV is read with Windows-1252 encoding.

## Dataset attribution

Source: [Superstore Dataset published by vivek468 on Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final). The CSV is included in `data/`; dataset rights and usage terms remain with the source.

## Validation status

Repository checks confirmed that both listed files exist, the PBIX archive passes its integrity check, and it contains report definitions, resources, and a data model. The report definitions reference the four measures above and the documented charts and slicers.

The included CSV has 9,994 rows and 5,009 distinct orders. Full-dataset reference totals calculated directly from the CSV are **2,297,200.86** in sales and **286,397.02** in profit. Clear report filters before comparing these totals with the report.

The DAX formulas, Power Query settings (including `CsvPath`, locale, and encoding), report rendering, interactions, and refresh have not been verified in Power BI Desktop during this repository check. The calculations and refresh instructions above remain subject to that verification.

