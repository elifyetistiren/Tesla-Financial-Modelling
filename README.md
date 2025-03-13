
# Tesla Financial Modeling Project

## 📌 Project Overview

This project presents a **comprehensive financial modeling and valuation analysis** of **Tesla Inc.**, integrating **data analytics techniques, financial forecasting, scenario modeling, and discounted cash flow (DCF) valuation.** The goal is to estimate Tesla’s fair stock price and business valuation by leveraging structured **financial data, predictive analytics, and comparative benchmarking.**

The model is built with **Excel-based financial analysis, structured scenario modeling, and dynamic sensitivity analysis** to ensure robust decision-making capabilities.

## 🔍 Key Data Sources & External Inputs

## 1. Drivers Sheet: Organizing External Inputs**

To streamline data management, the following categories of external inputs are incorporated into the **Drivers Sheet**:

### 1.1. Macroeconomic Assumptions
- **Ten-Year Treasury Yield**: Reflects the risk-free rate used in discounting future cash flows. The latest available rate (e.g., 0.697% as of September 18, 2020) is included and sourced from government or financial databases.
- **Market Risk Premium**: An industry-standard rate (e.g., 5%) used to estimate the expected return of equity investments.
- **Corporate Tax Rate**: The prevailing U.S. corporate tax rate (e.g., 21%) as of the model’s development.
- **Inflation Rate**: A long-term expected inflation rate (e.g., 2%) is applied to forecast future cost adjustments.

### 1.2. Company-Specific Inputs
- **Company Name & Currency**: The model is structured to dynamically update if another company is analyzed, though Tesla is the default.
- **Tesla’s Stock Beta**: As extracted from market sources such as Yahoo Finance (e.g., 2.15), used in CAPM calculations for the cost of equity.
- **Bond Yield**: Tesla’s bond yield as a proxy for the company’s cost of debt (e.g., 4.32%-4.4%).

### 1.3. Scenario Analysis Parameters
- **Scenario Selection**: A numerical input (1, 2, or 3) representing different business environments:
  - **1 – Best Case**: Optimistic revenue growth, low interest rates, and high demand.
  - **2 – Base Case**: Expected market conditions.
  - **3 – Worst Case**: Downturn scenario with reduced sales and higher costs.
- **Data Validation for Scenario Input**: Ensuring that the input field only accepts 1, 2, or 3 to prevent manual entry errors.

---

## 🚘 Tesla Vehicle Sales & Forecasting

### **2. Tesla’s Vehicle Models & Sales Projections**

Tesla currently offers Model S, Model X, and Model 3, with additional models planned:
- **Model Y** (Crossover SUV) - Production started in 2020.
- **Roadster 2** (High-performance sports car) - Expected in 2022.
- **Cybertruck & Semi** - Expected in 2021.

For baseline figures, **2019 deliveries** were **66,385** units for Model S/X and **300,815** units for Model 3. Initial estimates for new models are **500 units for Roadster 2 (2022) and 250 units for Cybertruck and Semi (2021).**

### 2.1 Growth Assumptions and Forecasting

- **New Models**: First 3 years follow Model 3’s rapid ramp-up, peaking at **60% growth**, then slowing to **10% (Years 4-5), 8% (Years 6-7), and 4% thereafter**.
- **Model S/X**: Given maturity, steady **4% growth** is assumed.
- **Model 3/Y**: Follows a trajectory similar to Model 3’s past growth.

Deliveries are projected by multiplying prior year figures by **(1 + growth rate)**. New model estimates follow an introduction ramp-up before stabilizing.
The **forecasting method** applies structured year-over-year percentage growth to **estimate Tesla’s vehicle deliveries** dynamically across the forecast period.

Historical data shows that Tesla’s strongest growth is projected between **2019 and 2023**, as new models enter the market. This is when Tesla is expected to surpass **1 million annual deliveries**. 

To gauge whether this is realistic, we compare Tesla’s expected deliveries with major global automakers:

- **Top competitors**: GM, Ford, Fiat-Chrysler, BMW, and Volkswagen, averaging **6.8 million vehicles per year**.
- **BMW, the smallest in the group**, delivers around **2.5 million vehicles annually**.
- **Tesla’s projection**: Expected to reach **1.8 million annual deliveries** within ten years.

---

## 💰 Revenue & Average Selling Price (ASP) Forecasting

### **3. Estimating Average Selling Price of Tesla Vehicles**

The ASP varies across different models and is influenced by factors such as pricing strategy, product mix, and market demand.

### 3.1 Calculation of ASP

Tesla’s ASP is derived using a weighted approach based on the expected sales mix of its models:
- **Model S/X**: Higher-end luxury vehicles, priced between **$85,000 - $110,000**.
- **Model 3/Y**: Mid-range models, priced between **$40,000 - $60,000**.
- **Roadster & Cybertruck**: Premium and commercial vehicles with varying price points.

### 3.2 Forecasting ASP Trends

- **Short-Term Outlook**: ASP is expected to decline slightly as Model 3 and Y constitute a larger share of deliveries.
- **Long-Term Stabilization**: The introduction of higher-end models like the Cybertruck and Roadster may balance the ASP.
- **Revenue Impact**: A declining ASP requires Tesla to sustain volume growth to maintain revenue momentum.

| Tesla Model | Price Range ($)      | Assumed ASP ($) |
| ----------- | --------------------- | ---------------- |
| Model S/X   | $85,000 - $110,000  | $102,000        |
| Model 3/Y   | $40,000 - $60,000   | $54,000         |
| Roadster 2  | $200,000 - $250,000 | $225,000        |
| Cybertruck  | $39,900 - $76,900   | $58,400         |
| Tesla Semi  | $150,000 - $200,000 | $175,000        |

## **4. Calculating Automotive Revenue**

Now that we have estimated the average price of each model and the respective number of deliveries, multiplying these numbers provides Tesla's expected automotive revenue.

Formula:**Revenue = Deliveries × ASP**Three scenarios adjust revenue:

- **Base Case:** 100% revenue forecast.
- **Worst Case:** 98% of base case.
- **Best Case:** 102% of base case.

A **CHOOSE function** dynamically updates revenue calculations based on the selected scenario.

---

## 📊 Gross Profit & Cost Analysis

### **5. Estimating Gross Profit % by Model**

We calculate Tesla’s automotive gross profit, determining how much of its revenue remains after production expenses. Given Tesla’s six vehicle types, we assign distinct gross profit percentages for each model rather than applying an average margin across all models.

### 5.1 Approach to Estimating Gross Profit %

- **Existing Models (Model S, X, and 3)**: Use Tesla’s historical gross profit margins for the last two years, as recent data better reflects current cost structures.
- **New Models (Model Y, Roadster, Cybertruck, Semi)**: Use industry comparisons, selecting three comparable automakers for each.

### 5.2 Comparable Analysis

- **Model 3 & Y**: Benchmarked against **GM, Ford, Fiat-Chrysler** with an average gross margin of **15.6%**.
- **Model S & X**: Compared to **BMW, Mercedes, Volkswagen**, with an average margin of **17%**.
- **Tesla Roadster**: Benchmarked against **Jaguar, Porsche, Ferrari**, yielding a premium margin of **44%**.
- **Other Models**: Adjusted based on **financial statements** of relevant peers.

Tesla’s **historic gross profit margin (22.3%)** outperforms its peer group. Applying peer-based margins ensures realistic projections for Tesla’s upcoming models. This approach enhances model accuracy and stability, accounting for Tesla’s evolving cost structure.

| Tesla Model       | Peer Companies            | Average Gross Margin (%) |
| ----------------- | ------------------------- | ------------------------ |
| Model 3/Y         | GM, Ford, Fiat-Chrysler   | 15.6%                    |
| Model S/X         | BMW, Mercedes, Volkswagen | 17%                      |
| Roadster 2        | Jaguar, Porsche, Ferrari  | 44%                      |
| Cybertruck & Semi | Industry Avg              | 20%                      |

	Multiply revenues by the selected gross profit percentage to get gross profit


## **6. Forecasting Cost of Sales**

With revenue and gross profit estimated, calculating Tesla’s cost of sales is straightforward.


Formula:**Cost of Sales = Revenue - Gross Profit**

- Cost structure adjusts for **best, base, and worst-case scenarios.**
- chart visualization highlights Tesla’s revenue (blue area) and gross profit (orange area).Tesla’s gross profit margin declined post-2017 as Model 3, with lower margins, gained prominence.
- The projected automotive gross profit margin is between **21% and 23%**.

### 6.1 Forecasting Energy and Services Revenue
To project Tesla’s revenue from energy generation, storage, and services, we rely on historical trends and apply a structured growth approach.

### 6.2 Revenue Growth Assumptions
- **2020**: 18% growth.
- **2021**: 12% growth.
- **2022**: 8% growth.
- **2023 onwards**: 6% annual growth.
- **Best Case**: +2% additional growth.
- **Worst Case**: -2% reduction from the base case.

### 6.3 Modeling Revenue Forecast
- The **CHOOSE** function allows for dynamic scenario selection.
- Each year’s revenue is calculated as: Previous Year Revenue × (1 + Growth Rate).
- Ensures flexibility and scalability across forecast periods.

## 6.4 Calculating Energy and Services Gross Profit and Cost of Sales

### 6.4.1 Gross Profit Assumptions
- Historically, these business lines have had **negative gross margins** (-9%).
- To maintain **cost neutrality**, we assume a **0% gross profit margin** going forward.
- **Scenario Adjustments**:
  - **Best Case**: Adds expected inflation rate.
  - **Worst Case**: Subtracts expected inflation rate.
  - Modeled using the **CHOOSE** function for flexibility.

### 6.4.2 Final Calculations
- **Gross Profit** = Revenue × Selected Gross Profit %.
- **Cost of Sales** = Revenue - Gross Profit (displayed as negative).

This ensures a **realistic and neutral forecast** for Tesla’s non-automotive business lines.

---

## 🚗 Operating Expenses, CapEx & Depreciation

### 7. Forecasting Operating Expenses (OpEx)

Operating expenses (OpEx) cover Tesla’s costs beyond cost of sales, including R&D, management, rent, utilities, sales, and advertising. Given Tesla’s rapid growth, we expect economies of scale to reduce OpEx as a percentage of revenue over time.

**Comparable benchmarking approach:**
- **Industry Average OpEx**: 14% of revenue.
- **Best Case**: 12% OpEx.
- **Worst Case**: 16% OpEx.

  Total OpEx = Revenue × Selected OpEx %.


A **CHOOSE** function allows OpEx adjustments based on selected scenarios.

### 7.1 Building Fixed Asset Roll Forward: PPE
Forecasting Property, Plant, and Equipment (PPE) is a key component of Tesla’s integrated financial model, linking the profit and loss statement (P&L) with the balance sheet through capital expenditures (CapEx), depreciation, and amortization.

### 7.1.1 PPE Forecasting Approach
- **Ending PPE = Beginning PPE + CapEx - Depreciation Expense.**
- Higher CapEx leads to increased PPE, while higher depreciation reduces PPE over time.
- The model maintains continuity by linking beginning PPE to prior period ending PPE.

### 7.1.2 CapEx Forecasting Scenarios
1. **Based on PPE Growth (Scenario 1):** CapEx is a function of beginning PPE, assuming slower amortization.
2. **Based on Revenue Growth (Scenario 2):** CapEx scales with revenue, assuming expansion requires new investments.


## 8. Estimating CapEx
Capital expenditures (CapEx) can be forecasted using two approaches: as a percentage of beginning PPE or as a percentage of revenue, suitable for high-growth companies.

### 8.1 CapEx Forecasting Methods
- **Scenario 1:** CapEx as a percentage of beginning PPE.
- **Scenario 2:** CapEx as a percentage of revenue.
- Outliers in industry comparables are removed for accurate benchmarking.

### 8.2 Scenario Adjustments
- **Best Case:** 5% lower than the base case for PPE-based CapEx, 3% lower for revenue-based CapEx.
- **Worst Case:** 5% higher than the base case for PPE-based CapEx, 3% higher for revenue-based CapEx.
- The CHOOSE function dynamically selects the appropriate scenario.

### 8.2 Final Calculation
- **CapEx = (Selected CapEx % × Beginning PPE) OR (Selected CapEx % × Revenue).**
- Formula applied across the 10-year forecast period.

---

## 9. D&A Schedule
The Depreciation and Amortization (D&A) schedule provides a structured approach to modeling asset depreciation, ensuring accurate financial forecasting.

### 9.1 D&A Calculation Approach
- **Depreciation of Historical Assets = Beginning PPE ÷ 10** (assumed 10-year useful life).
- **Depreciation of New CapEx = Each year’s CapEx ÷ 10,** applied cumulatively.
- Costs are recorded as negatives to align with financial modeling standards.

## 10. Calculating DSO, DIO, and DPO

Modeling Tesla’s **working capital components**—trade receivables, inventory, and trade payables—requires using the **Days technique**, a standard method in financial modeling.

### 10.1 Key Metrics, Forecasting Approach, and Final Calculation

- **Days Sales Outstanding (DSO):** Measures how long Tesla takes to collect receivables.
- **Days Inventory Outstanding (DIO):** Reflects how long inventory is held before being sold.
- **Days Payables Outstanding (DPO):** Indicates the time Tesla takes to pay suppliers.
- **Net Trade Cycle:** DSO + DIO - DPO

To forecast these metrics:
- **Use historical averages** to extend trends into the forecast period.
- **Apply the average function** to project days forward.
- **Fix column references** to ensure smooth formula replication.

With **DSO, DIO, and DPO forecasted**, trade receivables, inventory, and payables can be **reverse-calculated**, and a **panel output sheet** is prepared to organize results effectively.

---

## 11. P&L Output Sheet

The **Profit & Loss (P&L) output sheet** consolidates Tesla’s financial data, ensuring all key metrics are easily accessible.

### 11.1 Key Metrics, Forecasting Approach, and Final Calculation

- **Revenue** = Automotive Revenue + Energy Revenue.
- **Cost of Sales** = Automotive Cost of Sales + Energy Cost of Sales.
- **Gross Profit** = Revenue - Cost of Sales.
- **EBIT Calculation**: Links to **Operating Expenses (OpEx)** to determine earnings before interest and taxes.

To forecast these components:
- **Historical data is pre-filled**, ensuring consistency.
- **Formulas for 2020 are created**, allowing for easy application to future years.
- **Copy and paste methodology** extends calculations through **2029**, maintaining accuracy.

The **final calculation** ensures that all components are correctly linked to the **EBIT output**, which will drive further financial projections.

---

## 12. Investment in Working Capital

Managing **working capital investment** is essential for Tesla’s financial model, ensuring efficient use of resources across operations.

### 12.1 Key Metrics, Forecasting Approach, and Final Calculation

- **Revenue** = Automotive Revenue + Energy Revenue.
- **Cost of Sales** = Automotive Cost of Sales + Energy Cost of Sales.
- **Gross Profit** = Revenue - Cost of Sales.
- **Operating Expenses (OpEx)** are linked to derive EBIT.



The **final calculation** integrates these components into the **working capital schedule**, ensuring accurate tracking of Tesla’s short-term liquidity needs.

---



## 💵 Cash Flow Modeling & Valuation

## Forecasting Unlevered Free Cash Flow

To accurately forecast **unlevered free cash flow (UFCF)**, we derive Tesla’s **working capital components**—trade receivables, inventory, and trade payables—from estimated **days outstanding**.



## Key Metrics, Forecasting Approach, and Final Calculation

- **Trade Receivables** = (DSO × Revenue) ÷ 360
- **Inventory** = (DIO × Cost of Goods Sold) ÷ 360
- **Trade Payables** = (DPO × Cost of Goods Sold) ÷ 360 *(negative sign applied for balance sheet consistency)*

To forecast these components:
- **Link revenues and costs** to a single reference cell for consistency.
- **Copy and paste methodology** extends calculations through the forecast period.
- **Fixed references** ensure accuracy across all periods.

The **final calculation** ensures that these **working capital projections** are correctly factored into Tesla’s **cash flow analysis**.

---

## 13. Forecasting Other Assets

To complete Tesla’s **unlevered free cash flow (UFCF) forecast**, we incorporate **working capital investments, CapEx, and other assets & liabilities**.


### 9. Forecasting Unlevered Free Cash Flow (UFCF)
**Formula:**  
UFCF = EBIT - Taxes + D&A - CapEx - Working Capital Changes

# Steps to Calculate UFCF

## 1. Working Capital Adjustments
- **Trade Receivables:** Increased receivables mean **cash outflow** (subtract the change).
- **Inventory:** Similar to receivables, higher inventory means **cash outflow**.
- **Trade Payables:** Increased payables mean **cash inflow** (added to cash flow).

## 2. Incorporating CapEx & Other Assets
- **CapEx:** Added as a **negative cash flow** since it represents spending.
- **Other Assets:** Includes **restricted cash, prepaid expenses, leased assets, and intangibles**.

## 3. Other Liabilities
- Includes **accrued liabilities, deferred revenue, resale guarantees, and customer deposits**.

## 4. Final UFCF Calculation
- **Summing up** Gross Cash Flow, Working Capital Changes, CapEx, Other Assets, and Liabilities.

### Key Metrics, Forecasting Approach, and Final Calculation

- **EBIT** is sourced from the **P&L output sheet**.
- **Operating taxes** are determined using the **statutory tax rate** from the **Driver’s sheet**.
- **NOPAT (Net Operating Profit After Taxes)** is calculated as EBIT - Taxes.
- **Gross Cash Flow** is derived by adding back **non-monetary expenses (D&A)**.
- **Final UFCF** = Gross Cash Flow - Working Capital Investments - CapEx.


## 14. Forecasting Financing Activities


We start with **interest expense calculations**, using the **outstanding debt balance** and **assumed interest rates**. If Tesla issues new debt, we adjust the interest expense accordingly.

### Debt and Equity Financing:
- If **free cash flow is insufficient**, Tesla may raise funds through **additional borrowing** or **equity issuance**.
- The **debt roll-forward schedule** tracks **beginning debt, new borrowings, repayments, and ending balances**.

### Dividends and Share Buybacks:
- If Tesla generates **surplus cash**, it can **pay dividends** or **repurchase shares**, impacting the **equity portion** of the balance sheet.

### Final Adjustments:
- **Link net financing cash flow** to the **cash flow statement**.
- **Ensure total debt and equity financing** balance with **forecasted cash flows**.


## 15. Calculating Net Income

We derive **EBIT (Earnings Before Taxes)** and determine **income tax** using an **IF function**:
- **If EBIT > 0**, taxes = **EBIT × statutory tax rate**.
- **If EBIT ≤ 0**, taxes = **zero**.

Thus, **Net Income = EBIT - Taxes**. Minority interests are assumed to be zero.  
We then finalize the **cash flow statement** by bridging **unlevered free cash flow (UFCF)** with **net cash flow**.

We add **net cash flow** from the prior period to the existing cash balance. If calculations are correct, the **balance sheet balances**.




## 16. Weighted Average Cost of Capital (WACC) Calculation
**Formula:**  
WACC = (Debt/Total Capital) × Cost of Debt × (1 - Tax Rate) + (Equity/Total Capital) × Cost of Equity
- **Cost of Debt**: 4.3% (Tesla’s bond yield).
- **Cost of Equity (CAPM)**: Risk-Free Rate + Beta × Market Risk Premium.

# Cost of Debt & Cost of Equity Calculation

- **Cost of Debt**: Proxied using Tesla’s bond yield (**4.3% as of Sept 18, 2020**).
- **Cost of Equity**: Derived using the **Capital Asset Pricing Model (CAPM)**:
  - **Formula**:  
    \[
    \text{Cost of Equity} = \text{Risk-Free Rate} + \beta \times \text{Market Risk Premium}
    \]
  - **Risk-Free Rate**: 10-year US Treasury yield (proxy).
  - **Beta**: Measures Tesla’s stock volatility relative to the market.
  - **Market Risk Premium**: Assumed at **5%** based on historical averages.

### 16.1 WACC Calculation:
Using these values, **Weighted Average Cost of Capital (WACC)** is computed as:

\[
\text{WACC} = \left(\frac{\text{Debt}}{\text{Debt} + \text{Equity}}\right) \times \text{Cost of Debt} \times (1 - \text{Tax Rate}) + \left(\frac{\text{Equity}}{\text{Debt} + \text{Equity}}\right) \times \text{Cost of Equity}
\]

This equation accounts for both **cost of debt** (after-tax) and **cost of equity** in Tesla’s capital structure.


## 17. Discounted Cash Flow (DCF) Valuation
- **Discounted UFCF & Terminal Value** using **WACC**.
- **Terminal Value Formula:**  
  TV = (Final Year Cash Flow × (1 + g)) / (WACC - g)

# Discounting Cash Flows & Continuing Value

### 17.1 Discounting Cash Flows
- Unlevered cash flows are linked from the cash flow sheet.
- **Discount factor**: **Weighted Average Cost of Capital (WACC)**, considering both debt and equity holders.
- If interest expenses were deducted, we use the **cost of equity** instead.

### 17.2 Calculating Continuing Value
- **Perpetuity growth rate**: **2%**, aligning with long-term inflation.
- **Formula** for continuing value:
  
  \[
  \text{Final Year Cash Flow} \times (1 + g) / (\text{WACC} - g)
  \]

- All projected cash flows are **discounted to present value**.
- Each cash flow is **discounted using (1 + WACC) raised to the forecast year**.
- The **continuing value** is also **discounted** similarly.

### 18. Enterprise Value & Stock Price Estimation
**Formula:**  
Equity Value = Enterprise Value + Cash - Debt  
Stock Price = Equity Value / Shares Outstanding

With the present value of **forecasted cash flows** and the **continuing value**, we determine Tesla’s **enterprise value (EV)**.

- **Enterprise Value (EV)** = **Discounted cash flows** (forecast period) + **Discounted continuing value**.
- **Equity Value** = **EV + Cash - Financial Liabilities** (from balance sheet).
- **Price per Share** = **Equity Value / Outstanding Shares** *(932 million as of August 31, 2020).*

Comparing this **target price** with Tesla’s **market price** provides insights into **buying/selling opportunities**.  
This **DCF valuation** method helps assess Tesla’s **fair value** based on **fundamental financials**.



---



##  🔑 Key Issues Affecting Valuation:

### 1. Excessive CapEx Assumption
- The model assumes Tesla **continues investing 24%** of its existing **PPE annually**, indefinitely.
- This **unrealistic perpetual CapEx growth** lowers **unlevered free cash flow (UFCF)** and impacts **continuing value**.
- A **gradual reduction in CapEx investment** should be considered in later years.

### 2. Overestimated Other Liabilities
- **Other liabilities** are assumed at **20% of revenues**, but a comparison with **mature auto producers** would provide more realistic benchmarks.
- As **revenue growth stabilizes**, the **difference in other liabilities shrinks**, reducing **UFCF** towards the **final forecast years**.

### Why This Matters
- The **final projected year** is crucial since it **determines continuing value**, which accounts for **over half** of Tesla’s **enterprise value**.
- **Understated final-year UFCF** leads to a **lower equity valuation** than expected.


## 20. Key Insights & Findings
- Tesla’s projected revenue growth aligns with historical trends but faces risks from production scaling.
- Industry benchmarking validates Tesla’s target delivery volumes and gross profit margins.
- DCF-based valuation suggests significant market overpricing, requiring further sensitivity analysis.
- Scenario modeling provides insights into Tesla’s resilience under different economic conditions.

## 🎯 Final Summary of Tesla Financial Modeling Project

This marks the completion of our **Tesla valuation exercise**, where we developed a **DCF-based financial model** to estimate Tesla’s value.  
Throughout this process, we covered several **key aspects** of financial modeling, **valuation techniques**, and **forecasting methodologies**.

## Key Learnings from the Project:
- **DCF Valuation Model** – Understanding how **Discounted Cash Flow (DCF)** analysis works in **corporate valuation**.
- **Strategic Analysis** – Exploring various **strategy-based valuation enhancements**.
- **Financial Forecasting** – Implementing **Days methodology** for balance sheet projections.
- **Scenario Modeling** – Creating a **dynamic model** with multiple **financial scenarios**.
- **Cash Flow Analysis** – Constructing and analyzing a **cash flow statement**.
- **Unlevered vs. Net Cash Flow** – Distinguishing between the two and their **impact on valuation**.
- **Discounting Cash Flows** – Applying **Weighted Average Cost of Capital (WACC)** for **valuation accuracy**.
- **Continuing Value Estimation** – Projecting Tesla’s **long-term value** beyond the **forecast period**.
- **Sensitivity Analysis** – Evaluating how **different assumptions impact valuation results**.
- **Excel Applications** – Leveraging **advanced Excel tools** for **financial modeling**.
- **Data Presentation** – Using **professional formatting, charts, and visualizations** for insights.
- **Valuation Interpretation** – Understanding how our **model compares to market expectations**.

---

# Final Thoughts

By integrating **DCF valuation techniques, forecasting tools**, and **financial modeling best practices**, we successfully built a **comprehensive valuation model** for Tesla.  
This exercise **reinforces real-world financial analysis skills** and demonstrates the **importance of data-driven decision-making** in **investment valuation**.

✅ **Built with**: Excel, SQL (data extraction), Power BI (visualization), Financial Modeling Best Practices.


---



📧 **Contact:** *[elifyetistiren@gmail.com]*

---
