# India Agriculture Production Analysis (2010–2025)

## Year-wise Highest/Lowest by State and Trends

Author: [Your Name]
Institution: [Your Institution]
Date: [Update Date]

---

## Abstract
This report analyzes India’s agriculture across 28 states, 280 districts, and 25 crops from 2010–2025 (78,442 records). Using PySpark, we compute year-wise state rankings for average rainfall, fertilizer usage, total production, and total revenue, identify consistent leaders/laggards, and visualize long-term trends. Results show rising production and yield, relatively stable rainfall, and steady fertilizer usage. Revenue reflects production scale and crop price mix.

## 1. Objectives
- Year-wise Top/Bottom 10 states for: Avg Rainfall, Avg Fertilizer, Total Production, Total Revenue.
- Identify states in all Top-10 lists and states in none (per year).
- Show trends: production, yield, rainfall, fertilizer usage.
- Provide insights for planning and policy.

## 2. Dataset Overview
- Records: 78,442 (2010–2025)
- Geography: 28 States, 280 Districts
- Crops: 25
- Key columns: Year, State, Crop, Area_Hectares, Production_Tonnes, Yield_Kg_Per_Hectare, Rainfall_MM, Fertilizer_Usage_Kg_Per_Hectare, Market_Price_Per_Quintal

## 3. Methodology (Summary)
- Platform: PySpark (distributed aggregations).
- Revenue formula: Revenue = Production_Tonnes × 10 × Market_Price_Per_Quintal.
- Aggregation: Year × State for all four metrics; ranked Top/Bottom 10.
- Trends: Yearly totals/averages for production, yield, rainfall, fertilizer usage.

## 4. Global Results
- Total Production (2010–2025): 20,848,766,856 tonnes
- Total Cultivated Area: 2,000,595,618 hectares
- Overall Average Yield: 10,398.74 kg/ha
- Leading State (overall): Telangana — 793,462,889 tonnes; Avg Yield 10,742.46 kg/ha
- Top Crop (overall): Sugarcane — 6,626,986,533 tonnes; Avg Yield 80,727.47 kg/ha

> Note: Values above are computed from the provided dataset used in the notebook.

## 5. Year-wise Rankings (Insert for YOUR YEAR)
Replace YEAR with your focus year and paste tables/figures from the notebook.

- Highest Rainfall – Top 10 States (YEAR)
- Lowest Rainfall – Bottom 10 States (YEAR)
- Highest Fertilizer Use – Top 10 States (YEAR)
- Lowest Fertilizer Use – Bottom 10 States (YEAR)
- Highest Production – Top 10 States (YEAR)
- Lowest Production – Bottom 10 States (YEAR)
- Highest Revenue – Top 10 States (YEAR)
- Lowest Revenue – Bottom 10 States (YEAR)

Use in notebook:
- `show_rankings_for_year(YEAR)`
- `plot_year_overview(YEAR)`

## 6. Consistency Analysis (YEAR)
- States in all four Top-10 lists: [Paste list]
- States in none of the Top-10 lists: [Paste list]

Use in notebook: `compute_state_sets(YEAR)`

## 7. Trend Figures (2010–2025)
Paste exported images or screenshots from the notebook under these captions:
- Figure 1: Total Production Trend
- Figure 2: Average Yield Trend
- Figure 3: Average Rainfall Trend
- Figure 4: Fertilizer Usage Trend

Optional year visuals:
- Figure 5: YEAR Production Share among Top 10 States (Pie)
- Figure 6: YEAR Top 10 by Avg Rainfall (Bar)
- Figure 7: YEAR Top 10 by Avg Fertilizer (Bar)
- Figure 8: YEAR Top 10 by Revenue (Bar)

## 8. Insights and Discussion
- Production and Yield: Long-term rise; yield improvement is a key driver.
- Rainfall: Stable averages with inter-annual variability; localized extremes possible.
- Fertilizer: Stable near ~175 kg/ha; efficiency more impactful than higher dosage.
- Revenue Drivers: Production scale + crop price mix; high-value crops (e.g., spices) amplify revenue.
- Policy Suggestions: Precision inputs, irrigation efficiency, promote high-revenue crop mixes, support lagging states.

## 9. Limitations
- Prices are averages; intra-year/quality variation not modeled.
- State averages can mask district-level heterogeneity.
- Annual averages may not capture short-term shocks.

## 10. Conclusion
India’s agriculture shows strong gains in production and yield from 2010–2025 with steady fertilizer use and stable rainfall averages. Year-wise rankings highlight leaders and laggards, informing targeted policy actions and investment.

---

## Appendix A – How to Reproduce Tables/Figures
Run these in the notebook and paste outputs into this report:
- Rankings: `show_rankings_for_year(2025)`
- State Sets: `compute_state_sets(2025)`
- Year Overview Plots: `plot_year_overview(2025)`
- Trends: `plot_production_trend()`, `plot_yield_trend()`, `plot_rainfall_trend()`, `plot_fertilizer_trend()`

---

## Export Instructions
You can export this Markdown to PDF/DOCX/HTML.

### Option 1: Use VS Code / Cursor Markdown export
- Open `Major_Project_Report.md`
- Use “Export” or “Markdown: Print to PDF” extension/command to generate PDF.

### Option 2: Pandoc (DOCX/PDF/HTML)
- Install Pandoc. Then run in terminal from the project folder:
  - DOCX: `pandoc Major_Project_Report.md -o Major_Project_Report.docx`
  - PDF (needs LaTeX installed): `pandoc Major_Project_Report.md -o Major_Project_Report.pdf`
  - HTML: `pandoc Major_Project_Report.md -o Major_Project_Report.html`

### Option 3: Typora or Obsidian
- Open the `.md`, use built-in export to PDF/DOCX/HTML.
