Financial Reporting in Tableau - Part 2

In the previous part, we built our dashboard using filters. In this part, we will focus on using formulas and calculations to enhance our financial reporting in Tableau.

Calculations and Formulas

1. Sales Value Calculation:
   - Create calculated field: `Sales Value`
   - Formula: `SUM(IF [sub-class] = "sales" THEN [amount] ELSE 0 END)`

2. Gross Profit Calculation:
   - Create calculated field: `Gross Profit`
   - Formula: `SUM(IF [sub-class] = "profit" THEN [amount] ELSE 0 END)`

3. Operating Profit Calculation:
   - Create calculated field: `Operating Profit`
   - Formula: `SUM(IF [class] = "trading account" THEN [amount] ELSEIF [class] = "operating account" THEN [amount] ELSE 0 END)`

4. EBITDA (Earnings Before Interest, Tax, Depreciation, and Amortization) Calculation:
   - Create calculated field: `EBITDA`
   - Formula: `SUM(IF [subclass] = "sales" THEN [amount] ELSEIF [subclass] = "cost of sales" THEN [amount] ELSEIF [subclass] = "operating expenses" THEN [amount] ELSE 0 END)`

5. PBIT (Profit Before Interest and Tax) Calculation:
   - Create calculated field: `PBIT`
   - Formula: `SUM(IF [class] = "trading account" THEN [amount] ELSEIF [class] = "operating account" THEN [amount] ELSEIF [class] = "non-operating" THEN [amount] ELSE 0 END)`

6. Profit Margin Calculations:
   - Gross Profit Margin: `Gross Profit / Sales`
   - Net Profit Margin: `Net Profit / Sales`
   - Operating Profit Margin: `Operating Profit / Sales`

7. Marketing Expenses Calculation:
   - Create calculated field: `Marketing Expenses`
   - Formula: `SUM(IF [subclass] = "marketing" THEN [amount] ELSE 0 END)`

Dashboard Creation

1. Income Statement Dashboard:
   - Arrange year in columns and Gross Profit, Net Profit, Sales in rows.

2. Relationship Dashboard:
   - Rows: Sales / Marketing Expenses
   - Columns: Date (formatted for color)

3. Margin Analysis Dashboard:
   - Rows: Sales, Gross Profit, Net Profit
   - Columns: Date

Conclusion
By implementing these formulas and calculations in Tableau, we have created insightful dashboards for financial reporting. For further questions or assistance, feel free to reach out at moradiya9404@gmail.com.

