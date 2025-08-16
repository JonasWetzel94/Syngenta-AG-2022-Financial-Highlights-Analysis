# Syngenta AG — 2022 Financial Highlights Analysis (Excel)

## Visual Overview
<img width="740" height="549" alt="image" src="https://github.com/user-attachments/assets/e4d8fecf-645e-4c1c-af76-7c08e1aee583" />


## Case Description
You’re a financial analyst covering Syngenta AG. Using the company’s published 2022 report, you transfer the **Financial Highlights (Summary)** and related notes into Excel and analyze revenue drivers, profitability, liquidity, and equity movements using only public information. :contentReference[oaicite:0]{index=0}

## Tasks
- Locate Syngenta AG’s 2022 financial report (PDF) and extract statement data into Excel. :contentReference[oaicite:1]{index=1}  
- Build clean calculations for margins (gross/operating/net), ROA/ROE, and basic balance checks.  
- Summarize revenue drivers (volume, price, FX) and notable product/geography splits based on the report narrative & notes. :contentReference[oaicite:2]{index=2}  
- Provide a concise, recruiter-friendly deliverable explaining methods and results.

## Accounting/Analytics Steps
1. **Data capture from PDF → Excel**  
   - Copied the Financial Highlights table (2018–2022) into a structured Excel sheet; cleaned headings, number formats, and years. :contentReference[oaicite:3]{index=3}
2. **Core computations (2022)**  
   - Gross Profit = Sales − COGS = **8,323** (= 19,963 − 11,640).  
   - Operating Income = Gross Profit − Operating Expenses = **2,850** (= 8,323 − 5,473).  
   - Net Margin = Net Income / Sales ≈ **10%** (= 1,907 / 19,963).  
3. **Revenue analysis**  
   - FY22 revenue increased **~19%** vs. FY21: **+7% volume**, **+15% local prices**, **−4% FX**. :contentReference[oaicite:4]{index=4}  
   - Product example: **Seedcare +14%** YoY; **Flowers ≈ 1% of total** (197 / 19,963). :contentReference[oaicite:5]{index=5}
4. **Liquidity & financing notes**  
   - **CFO decreased** in FY22 vs. FY21; review cash flow statement narrative for drivers. :contentReference[oaicite:6]{index=6}  
   - Financing: repayments of private placement notes/leases and additional short-/long-term debt; annual dividends **$400m**. :contentReference[oaicite:7]{index=7}
5. **Controls**  
   - Reconcile statement subtotals and re-check margins; verify that **Assets ≈ Liabilities + Equity** (allowing for rounding/NCI presentation).

## Trial Balance / Data Summary (2022, USD $m)
> Source: “Financial Highlights (Summary)” screenshot.

| Line item                                   | 2022 |
|---|---:|
| Sales                                       | 19,963 |
| Cost of goods sold                          | (11,640) |
| **Gross profit**                            | **8,323** |
| Operating expenses                          | (5,473) |
| **Operating income**                        | **2,850** |
| Income before taxes                         | 2,242 |
| **Net income**                              | **1,907** |
| Net income attributable to Syngenta AG      | 1,909 |
| Current assets less current liabilities      | 3,720 |
| **Total assets**                             | **30,440** |
| Total non-current liabilities               | (9,530) |
| **Total liabilities**                        | **(23,517)** |
| Share capital                               | (6) |
| **Total shareholders’ equity**               | **(6,877)** |

**Checks**
- Gross Profit: 19,963 − 11,640 = **8,323** ✅  
- Operating Income: 8,323 − 5,473 = **2,850** ✅  
- Net Margin: 1,907 / 19,963 = **9.6% ≈ 10%** ✅  
- Balance check: 23,517 + 6,877 = **30,394** vs. assets **30,440** (≈ rounding/NCI presentation).  

## Financial Statements / Results (Key Ratios, 2022)
- **Gross profit margin:** **42%**  
- **Operating profit margin:** **14%**  
- **Net profit margin:** **10%**  
- **ROA:** **7%**  
- **ROE:** **31%**  

_Note: Ratio labels and values reflect the company’s summary table; reproduce exactly in Excel for consistency._

## Mapping / Logic
- **Income Statement mapping**
  - `Gross Profit = Sales – COGS`
  - `Operating Income = Gross Profit – Operating Expenses`
  - `Net Income` taken directly from highlights table (to avoid double-adjusting interest/taxes baked into EBIT-to-NI bridge).
- **Margins**
  - `Gross Margin = Gross Profit / Sales`
  - `Operating Margin = Operating Income / Sales`
  - `Net Margin = Net Income / Sales`
- **Balance Sheet linkage**
  - Validate `Total Assets ≈ Total Liabilities + Total Equity` (small gaps acceptable due to rounding or non-controlling interests presentation).
- **Revenue drivers (narrative → numbers)**
  - From report text: `ΔRevenue% = Volume% + Price% + FX%` = `7% + 15% − 4% ≈ 19%`. :contentReference[oaicite:8]{index=8}

## How I Built It
- **Tools:** Excel (clean sheets, cross-checks), PDF-to-Excel copy with structure clean-up. :contentReference[oaicite:9]{index=9}
- **Excel techniques (examples)**  
  - Cleaning pasted rows: `=TEXTSPLIT(raw_text,CHAR(9))` or `Data → Text to Columns`.  
  - Core math: `=Sales - COGS`, `=GrossProfit / Sales`.  
  - Consistent formatting: custom number format for parentheses; percentage with one decimal.  
  - Control cells:  
    ```excel
    =ROUND(TotalLiabilities + TotalEquity - TotalAssets,0)   // should be ~0
    =ROUND(NetIncome / Sales, 4)                              // net margin
    ```
- **Documentation:** comments next to each formula; a small “Checks” section at the top of the sheet to show all-green status.

## What I Learned
- Fast, reliable extraction of statement data from PDFs into Excel with minimal manual fixes. :contentReference[oaicite:10]{index=10}  
- Translating MD&A narratives (volume/price/FX, product lines) into simple, auditable calculations. :contentReference[oaicite:11]{index=11}  
- Building quick integrity checks (subtotals, margin math, and assets vs. liabilities+equity).


## Quick Skills Snapshot
- Financial statement extraction & reconciliation (PDF → Excel) with robust checks. :contentReference[oaicite:12]{index=12}  
- Margin/return analysis (GM, OM, NM, ROA, ROE) reproduced from issuer data.  
- Revenue driver translation (volume/price/FX) from MD&A into simple analytics. :contentReference[oaicite:13]{index=13}  
- Clean, hiring-manager-friendly documentation and visuals aligned to the source.

