## Medicare Part D Prescribing Cost Analysis

### Question
Which states and territories are most underserved by Medicare providers, and which specialties drive the greatest access gaps?

### Data Source
CMS Medicare Part D Prescribers by Provider and Drug
[2023] — ~25M records, publicly available at data.cms.gov

### Tools
DuckDB · Python (pandas, plotly, seaborn) · Tableau Public

### Key Findings
- There are over 700 times where a state has only one CMS provider for a specialty. States like California and Florida have over 25 specialties with only one provider for the whole state.
- Puerto Rico has 7 specialty shortfalls relative to the national average. The gaps are deepest in physicial assistants and nurse practioners, where the territory would need an estimated 1000 and 2100 additional providers respectively to reach parity. This shortfall coincides with above-average cost-per-claim in the affected specialties: Beneficiaries in PR spend nearly 3000 dollars more per claim than the national average.


### Tableau Dashboard
[Link to Tableau Public]

### Methodology
The hypothesis for this analysis is that access gaps and cost burdens tend to co-occur in underserved territories. Provider distribution was analyzed across all 50 states and U.S. territories using a location quotient framework, which measures the ratio of actual providers in a given state to the number that would be expected based on that state's share of the total provider population. Location quotients below 1.0 indicate underrepresentation relative to the national baseline. To identify statistically significant access gaps rather than minor variation, outlier detection was applied specialty-by-specialty using the interquartile range method: states falling more than 1.5 times the IQR below the first quartile for a given specialty were flagged as underserved. This approach surfaces meaningful distributional anomalies while remaining robust to the wide variation in provider counts across specialties. Geographic findings were then cross-referenced with cost-per-claim data from the Part D prescriber-drug dataset, comparing state-level averages against national specialty benchmarks to assess whether provider shortfalls coincide with elevated drug costs. 
