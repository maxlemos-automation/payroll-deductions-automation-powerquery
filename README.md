# 📌 Payroll Deductions Automation (Power Query Version)

![Power Query](https://img.shields.io/badge/Power%20Query-M%20Language-FFD000?style=for-the-badge&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel-Automation-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge)

## 📍 Project Overview
This project automates the ETL (Extract, Transform, Load) process of employee deduction data into a payroll-ready format for the **Metiri ERP system**, using **Microsoft Power Query**.

It reads raw Excel input files, reshapes the data, applies deduction code mapping, and produces a structured dataset ready for `.txt` export and system import.

---

## ⚙️ What the automation does
- **Extracts:** Imports raw Excel files with employee deductions (unstructured).
- **Cleans:** Standardizes fields (handling missing values, numeric formats).
- **Transforms:** Converts data from human-readable **wide layout** to machine-readable **long layout** (Unpivoting).
- **Maps:** Translates deduction names to specific payroll system codes (e.g., "Gym" → "DED_005").
- **Enriches:** Adds payroll metadata (settlement dates, installments).
- **Loads:** Produces a final table ready for semicolon (`;`) separated export.

---

## 📂 Project Structure

| File | Description |
|------|-------------|
| `PowerQuery_PayrollAutomation.xlsx` | **Core File.** Contains all Power Query (M) logic and UI. |
| `employee_deductions_sample.xlsx` | Example input file (Anonymized Data). |
| `deduction_codes.xlsx` | Mapping Table: Deduction Name → System Code. |
| `example_output.xlsx` | Preview of the final dataset generated. |

---

## 🛠 Tech Stack
- **Microsoft Excel 365**
- **Power Query (M Language)** for Data Transformation.

---

## ▶️ How to use

1. Open `PowerQuery_PayrollAutomation.xlsx`.
2. Place the input files (`employee_deductions_sample.xlsx` + `deduction_codes.xlsx`) inside a known folder.
3. Update the **Config Table** in the Excel sheet (or Edit Parameters in Power Query):
   - `FilePath_Deductions`
   - `FilePath_CodeMapping`
   - `StartDate` / `FinalDate`
4. Go to **Data tab → Refresh All**.
5. The `Final Output` table will update automatically. Copy and paste it into a `.txt` or `.csv` file.

### 🛠️ Configuration Example

Ensure your paths are correct in the Config table.
*Note: Use absolute paths for stability.*

```text
| Parameter           | Value                                      |
|---------------------|--------------------------------------------|
| deduction_codes     | C:\Users\Max\Documents\Payroll\codes.xlsx  |
| employees_deduction | C:\Users\Max\Documents\Payroll\input.xlsx  |
| start_date          | 01/01/2025                                 |
| final_date          | 15/01/2025                                 |


