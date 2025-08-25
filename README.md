# 📑 Advanced PDF Invoice Processing & Reporting Automation 🤖  

![UiPath](https://img.shields.io/badge/Made%20with-UiPath-blue)  
![Excel](https://img.shields.io/badge/Excel-Automation-green)  
![Status](https://img.shields.io/badge/Status-Completed-success)  
![License](https://img.shields.io/badge/License-Nishant-yellow)  

---

## 📌 Overview
A **UiPath RPA Bot** that automates the complete cycle of **invoice processing**:  
- Extracts details from PDF invoices (both text-based & scanned)  
- Validates the data  
- Writes clean records into Excel trackers  
- Generates monthly vendor reports  
- Handles errors & archives completed files  

This project demonstrates how **automation can transform financial workflows** by reducing manual effort, improving accuracy, and saving time.  

---

## 🗂 Folder Structure
The bot works with three main folders:  

- 📂 **Input** → Contains all new invoices (PDFs) to be processed  
- 📦 **Archive** → Stores all successfully processed invoices  
- ⚠️ **Error** → Stores problematic invoices that failed during processing  

*(Sample PDFs are included inside the **Input** folder for testing.)*  

---

## 📊 Excel Outputs
The bot generates and maintains three Excel files:  

1. **Records.xlsx** → Master tracker containing all successfully processed invoices  
2. **Records_Error.xlsx** → Log of invoices that failed validation (e.g., missing fields, invalid data)  
3. **Monthly_Salary.xlsx** → Vendor-wise monthly summary report (calculated using loops, without pivots)  

---

## 🔍 Process Flow
Here’s the complete step-by-step workflow:  

1. **Scan Input Folder** → Reads all invoice PDFs inside *Input*  
2. **OCR + Regex Extraction** → Extracts Invoice Number, Date, Vendor, and Amount  
3. **Validation Rules Applied** →  
   - Amount must be greater than 0  
   - Date must be in correct format  
   - All key fields must be present  
4. **Valid Invoices → Records.xlsx**  
5. **Invalid Invoices → Records_Error.xlsx**  
6. **Generate Monthly Report → Monthly_Salary.xlsx** using For Each Row loop  
7. **Move Valid PDFs → Archive folder**  
8. **Move Invalid PDFs → Error folder**  
9. **Log Errors** → All issues recorded for review  

---

## ⚙️ Tech Stack
- **UiPath Studio** 🤖 (OCR, Regex, Excel, File Handling)  
- **Excel** 📊 (Master Records, Error Log, Monthly Summary Report)  
- **Document Understanding Framework** 📝  
- **Validation & Exception Handling** ⚡  

---

## 🚀 Impact
- ⏳ Reduced processing time **from hours ➝ minutes**  
- ✅ Eliminated manual errors with **automated validation**  
- 📊 Vendor-wise monthly reporting generated dynamically  
- 🔄 Built a **scalable, reusable, and efficient automation bot**  

---

## 🌟 Key Learnings
- Hands-on with **OCR & Regex** for unstructured PDF data  
- Implemented **For Each Row loops** for reporting (without pivot tables)  
- Applied **Exception Handling** for error-proof automation  
- Understood how **RPA can streamline finance & accounting processes**  

---

## ▶️ How to Run This Bot

### 1. Clone or Download Repository
```bash
git clone https://github.com/your-username/pdf-invoice-automation.git
