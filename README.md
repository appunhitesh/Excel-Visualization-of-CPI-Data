# Excel-Visualization-of-CPI-Data
Developed an end-to-end Excel data analysis project examining historical Consumer Price Index (CPI) trends from 2017 to 2023. The project involved data cleaning, transformation, and the categorization of complex economic metrics into broader, actionable categories to uncover macroeconomic inflation patterns and deliver clear visual insights.

# India CPI Inflation Analysis (2013–2023)

Analysis of India's All-India Consumer Price Index (CPI, base 2012 = 100) across Rural, Urban and Combined sectors. The project cleans the raw index data, computes year-over-year (YoY) inflation, and produces dashboard-ready tables for four problem statements.

## Problem statements

1. **Category contribution** – How much does each broad category (Food, Housing, Fuel & light, etc.) contribute to the basket and to inflation?
2. **YoY inflation trends** – How has inflation moved over time, and which year had the highest inflation?
3. **COVID-19 impact** – How did inflation behave before, during and after the pandemic?
4. **Oil and global events** – How did oil price swings and events such as the Russia–Ukraine war show up in fuel, transport and headline inflation?

## Dataset

- **File:** `data/All_India_Index_Upto_April23.csv`
- **Coverage:** Jan 2017 – May 2023, three sectors (Rural, Urban, Rural+Urban), 372 rows × 30 columns
- **Columns:** Sector, Year, Month, 12 food sub-groups, 6 major groups, 8 non-food sub-groups and the General index
- **Values:** Index numbers (2012 = 100), not prices or percentages


## Method

- **YoY inflation** = (Index_t / Index_t−12 − 1) × 100
- **Annual inflation** = average of the available monthly YoY values in the year
- **Contribution to inflation** = effective weight × group YoY, where effective weight = w_i·I_i,t−12 / Σ w_j·I_j,t−12. Contributions sum to headline YoY within about 0.04 percentage points.

## Repository contents

| File | Description |
|---|---|
| `All_India_Index_Upto_April23.csv` | Raw CPI index data |
| `CPI_Visuals.xlsx` | Cleaned data and one set of sheets per problem statement (see below) |

## Assumptions and limitations

- Basket weights (MoSPI CPI-2017 combined series) are not in the dataset; they were added from external knowledge.
- The dataset has no crude-oil price series. Links to oil and global events are inferred from Fuel & light and Transport & communication inflation plus general context.
- 2023 covers only Jan–May. Some 2019–2021 averages use fewer months because of the missing data above.

## Tools

Excel (formulas).

## License

Add your preferred license (e.g. MIT). The CPI data originates from India's Ministry of Statistics and Programme Implementation (MoSPI); check its terms of use before redistributing.
