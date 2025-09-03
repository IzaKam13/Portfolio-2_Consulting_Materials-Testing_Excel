# R&D Consulting in Materials Testing - Portfolio Project

This project showcases an end-to-end workflow for merging messy lab exports, normalizing units, enriching with metadata, applying spec limits, and building a refreshable dashboard with **Excel**.
It simulates a customer implementation scenario in an R&D lab, where instrument outputs are inconsistent and require cleaning before being useful for KPI tracking.


## Objectives

- Combine 3 monthly CSV exports with different delimiters, headers, and decimal formats.
- Normalize temperature, pressure, tensile, viscosity, and conductivity into canonical units.
- Enrich results with sample metadata (material, batch, project).
- Apply spec limits per (Material + TestType) and calculate Pass/Fail.
- Build an interactive dashboard (PivotTables + slicers).
- Flag data quality issues (impossible values, mislabeled units, low-variance parameters).


## Project Structure

<img width="382" height="271" alt="image" src="https://github.com/user-attachments/assets/f6b87c76-a614-4079-a122-03441b1760bd" />


## Dashboard

- Average Results by Material and TestType
- Pass/Fail counts by Month and Material
- Error analysis (% outliers per TestType, unit issues)
- Interactive slicers for Material, TestType, Month, Pass/Fail

![dashboard](https://github.com/IzaKam13/Portfolio-2_Materials-Testing_Excel-Python/blob/main/docs/Dashboard.png)


## Data Quality Findings & Open Questions

**1. Units** – Different canonical units per TestType (MPa, Pa·s, S/m). Added a legend for clarity.
**2. Temperatur**e – Some values near 0 K (likely mislabeled °C). Requires customer confirmation.
**3. Pressure** – Nearly constant across tests, adds little value; excluded from plots.
**4. Outliers** – Extremely large numbers (e.g., 2.7E+308) flagged as anomalies; excluded from KPIs.
**5. Spec Limits** – Assumed constant per Material/TestType; may need refinement by batch or instrument.


## Tools & Skills Demonstrated

- **Excel 2016**: Power Query, PivotTables, slicers, conditional formatting
- **Data Cleaning**: VLOOKUP (multi-key via helper columns), text normalization, missing data handling, trimming, unifying names of columns in different tables
- **R&D Context**: Unit conversions, spec-based QC, traceability of anomalies
- **Consulting Mindset**: Documenting assumptions, surfacing issues to customer, not “fixing silently”


## License

This project is licensed under the MIT License.
