# BEVERAGE SALES ANALYSIS USING MYSQL AND EXCEL

![Beverage Sales Analysis](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*WNTneKaklgnIOh3G7w8c7w.png)


# PROBLEM STATEMENT

Some Beverage companies, leading distributor of consumer products, was facing a pressing issue — inconsistent sales performance across different regions. 
While some areas thrived, others lagged behind, causing a disconnect between budgeted and actual sales. Profit margins fluctuated, and managers struggled to pinpoint the root causes behind the underperformance.

Company executives grew concerned. Were certain products not performing well? Were sales managers assigned inefficiently? Was regional demand being misjudged? Without concrete data-driven insights, decision-making felt like a guessing game.

To tackle this, they turned to their data analytics team, seeking clear, actionable insights that could help them identify trends, optimize sales strategies, and boost profitability across all regions. The challenge was set — could data unlock the secrets behind their sales struggles?


![](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*n1NVeHXGSvcwan3lQLhRIw.png)

# DATA MODEL

![Data Model](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*XZ9aMgNtZSlTfHRM8ydUbg.png)


# ANALYSIS:


### 1.Market Share of Each Company

**SQL QUERY**
```sql

SELECT o.company,
       ROUND((SUM(o.units_sold) / (SELECT SUM(units_sold) FROM orders)) * 100, 2) AS market_share
FROM orders o
GROUP BY o.company;

```


Output:

![Market Share Of Each Company](https://miro.medium.com/v2/resize:fit:498/format:webp/1*GKQRYyIxEpdDr3s993S0tA.png)

Visualization :

![Market Share Of Each Company](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*nUUB9JzqBMEEK4hTVgNKyw.png)










