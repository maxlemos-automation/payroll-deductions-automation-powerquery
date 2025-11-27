# 📌 Payroll Deductions Automation (Power Query Version)

## 📍 Project Overview
This project automates the transformation of employee deduction data into a payroll-ready format for the **Metiri payroll system**, using **Microsoft Power Query** in Excel.

It reads raw Excel input files, reshapes the data, applies deduction code mapping, and produces a structured dataset ready for TXT export and system import.

---

## ⚙️ What the automation does
- Imports a source Excel file with employee deductions  
- Cleans and standardizes fields (missing values, numeric formats)
- Converts data from **wide → long** layout
- Maps deduction names to payroll system codes
- Adds payroll metadata (date range, quantity, installment)
- Produces a table ready for `.txt` export (semicolon `;` separated)

---

## 📂 Project Structure

| File | Description |
|------|-------------|
| `PowerQuery_PayrollAutomation.xlsx` | Contains all Power Query logic and UI configuration |
| `employee_deductions_sample.xlsx` | Example input file (anonymized test data) |
| `deduction_codes.xlsx` | Mapping: deduction → payroll system code |
| `example_output.xlsx` | Example final dataset exported from the query |

> File names can be updated based on your structure in GitHub.

---

## 🛠 Tech Stack
- **Microsoft Excel**
- **Power Query (M Language)**

---

## ▶️ How to use

1. Open `PowerQuery_PayrollAutomation.xlsx`
2. Place the input files (`employee_deductions_sample.xlsx` + `deduction_codes.xlsx`)
   inside the same folder
3. Update the **Config Sheet** fields:
   - `FilePath_Deductions`
   - `FilePath_CodeMapping`
   - `StartDate`
   - `FinalDate`
4. Go to **Data → Refresh All**
5. Review the `Final Output` table and export it to `.csv` using semicolon delimiters

---

## 🔒 Privacy & Authenticity
This automation is based on a **real payroll workflow** implemented in production.  
All employee personal data has been fully anonymized.  
Original Spanish business terminology is preserved to maintain usability and authenticity.

---

## 🚀 Future Improvements
- Direct TXT export using VBA or Office Scripts
- Validation checks for missing deduction codes
- Improved parameter UI for date selection

---

## 👤 Author
**Max Lemos — Data Automation & Analytics**  
🔗 GitHub Profile: https://github.com/maxlemos-automation


