# SDG Funding Patterns Analysis for India (2000–2021)

## Authors
**Aarushi Shastri**
**Eeshanya Shahjee**  
Bharati Vidyapeeth (Deemed to be University), College of Engineering, Pune  
Department of Computer Science and Business Systems  
**Faculty Mentor**: Prof. Bindu Garg

## Project Description
This project presents a comprehensive data visualization of Official Development Assistance (ODA) directed toward the Sustainable Development Goals (SDGs) in India from 2000 to 2021. Using Power BI, Python, and Excel, we developed an interactive, multi-page dashboard to analyze financial flows from global donors to India's SDG-aligned development efforts.

The analysis leverages two authoritative datasets from AidData, capturing both project-level and aggregated SDG funding. Processed and standardized data enables users to explore historical trends, donor priorities, and goal-specific funding gaps over a 21-year period.

## Key Objectives
- Identify funding trends across two decades.
- Analyze SDG-specific investment priorities.
- Highlight funding gaps and donor preferences.
- Enable data-driven policymaking and accountability.

## Data Sources
### Financing to the SDGs Dataset (2000–2013)
- https://www.aiddata.org/data/financing-to-the-sdgs-dataset
  
- ##**Summary:**
- Provides project-level data on estimated Official Development Assistance (ODA) commitments to the 17 Sustainable Development Goals (SDGs) from 2000 to 2013.
- Tracking more than $1.5 trillion in financing cross-walked to the SDGs from 1.2 million ODA projects in AidData's Core Research Release 3.1.
  
- ##**Citation**:
- Sethi, T., Custer, S., Turner, J., Sims, J., DiLorenzo, M., & Latourell, R. (2017). Realizing Agenda 2030: Will donor dollars and country priorities align with global goals? Williamsburg, VA: AidData at the College of William & Mary.
  
- ##**Date Published:**
- November 6, 2017

### Financing the 2030 Agenda Dataset (2010–2021)
- https://www.aiddata.org/data/financing-the-2030-agenda-for-sustainable-development-version-1-0
  
- ##**Summary:**
- Disbursements from 157 DAC and non-DAC donors between 2010 and 2021 as captured by the OECD CRS Database. Aggregated by year, donor, and recipient.

- ##**Citation:**
- Burgess, B., Bengtson, A., and B. Lautenslager. (2023). Financing the 2030 Agenda for Sustainable Development, Version 1.0. Williamsburg, VA. AidData. Accessed at http://aiddata.org/sdg

- ##**Date Published:**
- October 16, 2023

## Methodology
### Data Processing Pipeline
Harmonized two differently structured datasets into a single, India-specific dataset for Power BI analysis.

#### Steps:
1. **Data Extraction & Filtering**
   - Loaded .xlsx files and extracted records where India was the recipient country.
2. **Format Harmonization**
   - Aggregated 2000–2013 project-level data to year/donor/SDG level.
   - Matched structure to the 2010–2021 aggregated dataset.
3. **Donor Standardization**
   - Mapped donor names to numeric codes for consistency.
4. **Metrics Calculation**
   - Total Disbursement and SDG Disbursement sums.
   - Derived Non-SDG Funding (Total – SDG Disbursement).
5. **Export & Dashboard Integration**
   - Cleaned, renamed, and reordered columns.
   - Exported a final dataset for Power BI visualization.

#### Tools:
- Python (pandas for preprocessing)
- Microsoft Excel (validation/aggregation)
- Power BI (interactive dashboards)

## Python Script Description
A custom Python script was developed using **Google Colab** to automate the extraction, preprocessing, aggregation, and standardization of the AidData datasets.

Key functionalities of the script include:
- Uploading .xlsx datasets interactively using Google Colab.
- Mapping donor names to standardized numeric donor codes for consistency.
- Aggregating funding data by year, donor, and recipient country.
- Calculating derived financial metrics including Total Disbursement, SDG Disbursement, and Non-SDG Funding.
- Reformatting the cleaned dataset to be directly compatible with Power BI ingestion.
- Exporting the processed dataset as a downloadable Excel file for dashboard creation.

This ensured that the preprocessing workflow was replicable, accurate, and aligned with the dashboard's data modeling needs.

## Power BI Dashboard Features
### Pages:
1. **Home**: Overview and navigation.
2. **Year-Wise Trends**: Disbursement patterns and project volume.
3. **Donor-Wise Analysis**: Contributions by organization.
4. **Goal-Wise Analysis**: Investment across SDGs 1–17.
5. **Summary & Insights**: Key trends, gaps, and findings.

### Visualizations:
- KPI cards
- Line/bar charts
- Tree maps
- Matrix tables
- Dynamic slicers (Year, Donor, SDG Goal)

## Outcomes
- Created a consistent, comparable dataset (2000–2021).
- Revealed top donors, trends, and underfunded SDGs for India.
- Delivered a decision-support tool for:
  - Policymakers
  - Researchers
  - Donor agencies
  - Development analysts

## License
For academic and educational use.  
Please cite AidData datasets when referencing or extending this work.
