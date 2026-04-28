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
//Brief paragraph on outlier detection approach.//
