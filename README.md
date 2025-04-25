
# SDG Funding Patterns Analysis for India (2000–2021)

This project presents an interactive Power BI dashboard analyzing Official Development Assistance (ODA) committed to the Sustainable Development Goals (SDGs) in India from 2000 to 2021. It is based on donor disbursement data extracted from two publicly available global datasets curated by AidData. The analysis enables exploration of long-term investment trends, donor behavior, goal-specific funding, and funding gaps in India’s development financing landscape.

---

## 📂 Data Sources

### 1. [Financing to the SDGs Dataset (2000–2013)](https://www.aiddata.org/data/financing-to-the-sdgs-dataset)
> *AidData, Core Research Release 3.1*

- Tracks project-level SDG-related commitments from 2000–2013.
- Contains over 1.2 million projects, estimating over $1.5 trillion in financing.
- Used to extract India-specific records from raw project-level data.

**Citation:**
> Sethi, T., Custer, S., Turner, J., Sims, J., DiLorenzo, M., & Latourell, R. (2017). *Realizing Agenda 2030: Will donor dollars and country priorities align with global goals?* Williamsburg, VA: AidData.

---

### 2. [Financing the 2030 Agenda Dataset (2010–2021)](https://www.aiddata.org/data/financing-the-2030-agenda-for-sustainable-development-version-1-0)
> *Version 1.0, OECD CRS-based Aggregation*

- Covers disbursements from 157 DAC and non-DAC donors between 2010–2021.
- Data aggregated by year, donor, and recipient country.

**Citation:**
> Burgess, B., Bengtson, A., & Lautenslager, B. (2023). *Financing the 2030 Agenda for Sustainable Development, Version 1.0.* Williamsburg, VA: AidData. Available at: https://aiddata.org/sdg

---

## 🔧 Data Processing Pipeline

We combined the two datasets and filtered for India as the recipient. All transformations were done using Python, Excel, and Power BI:

### 🔁 Python Script Steps

1. **File Upload & Loading**:
   - Reads raw or summarized `.xlsx` files.
   - Extracts India-specific donor records.

2. **Donor Code Mapping**:
   - Uses a dictionary to convert full donor names (e.g., "USA", "UNICEF") into standardized numeric codes.

3. **Data Aggregation**:
   - Aggregates by year, donor, and recipient.
   - Calculates:
     - Total Disbursement (USD)
     - Total SDG Disbursement (USD)

4. **Derived Metrics**:
   - Total Non-SDG Funding = Total Disbursement – SDG Disbursement
   - Total Environmental/Non-SDG Funding = Derived placeholder for environmental earmarks.

5. **Standardization & Export**:
   - Renames columns for Power BI
   - Reorders columns
   - Exports final file as Excel for visualization

---

## 📊 Power BI Dashboard Features

- Multi-page Interactive Dashboard (5 pages):
  - Home (Overview + Navigation)
  - Year-wise Disbursement Trends
  - Donor-wise Insights
  - Goal-wise SDG Funding Patterns
  - Summary of Key Findings

### Key Visualizations:
- Bar and line charts (trends)
- KPI cards (top donors, peak years)
- Tree maps (goal funding)
- Matrix tables (donor-goal funding intersections)
- Slicers (Year, Donor, SDG Goal)

---

## 💡 Outcomes

- Identified India’s top development partners and their preferred SDGs.
- Analyzed shifts in funding trends between 2000–2013 and 2010–2021.
- Visualized donor diversity, sector focus, and potential underfunded goals.
- Created a ready-to-use dashboard for policy analysis, research, or development planning.

---

## 👥 Authors

- **Aarushi Shastri**
- **Eeshanya Shahjee**
- *Bharati Vidyapeeth (Deemed to be University), College of Engineering, Pune*
- *Department of Computer Science and Business Systems*

**Faculty Mentor:** Prof. Bindu Garg

---

## 📎 License

This project is for academic and educational purposes. Please cite the original AidData datasets if using the content for research or policy work.
