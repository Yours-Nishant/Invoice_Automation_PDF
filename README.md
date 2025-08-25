# 📑 Advanced PDF Invoice Processing & Reporting Automation 🤖  

![UiPath](https://img.shields.io/badge/Made%20with-UiPath-blue)  
![Excel](https://img.shields.io/badge/Excel-Reporting-green)  
![Status](https://img.shields.io/badge/Status-Completed-success)  
![License](https://img.shields.io/badge/License-Nishant-yellow)  

---

## 📌 Overview  
This project automates the **processing of invoices from PDF files** and generates **monthly vendor reports** using UiPath Studio.  

The bot extracts data such as **Invoice Number, Date, Vendor Name, and Amount**, validates entries, writes them into an Excel tracker, calculates monthly totals, and generates structured summary reports. It also handles errors and archives processed files automatically. 🚀  

---

## 🔍 The Problem  
- Accountants spend hours manually processing invoices every month.  
- Manual entry is **time-consuming**, **error-prone**, and **repetitive**.  
- Generating monthly vendor reports requires repetitive Excel tasks.  
- Archiving and error handling increase workload.  

---

## 💡 The Solution  
The UiPath workflow solves these challenges by:  
1️⃣ Reading both **text-based & scanned PDFs**  
2️⃣ Extracting key fields with **OCR + Regex**  
3️⃣ Validating data (e.g., Amount > 0, Date format)  
4️⃣ Writing records into a **Master Excel Tracker**  
5️⃣ Using **For Each Row loops** to calculate vendor-wise monthly totals  
6️⃣ Generating **summary reports** in Excel  
7️⃣ Archiving successfully processed invoices  
8️⃣ Logging errors for unprocessable files  

---

## 🛠️ How It Works (Step-by-Step)  
1. 📂 **Folder Scan** → Reads all PDFs from the *Input* folder  
2. 🔍 **OCR + Regex** → Extracts fields (Invoice No, Date, Vendor, Amount)  
3. 🧮 **Validation** → Ensures values are correct  
4. 📊 **Excel Write Range** → Updates Master Excel Tracker (Records.xlsx)  
5. 🔄 **For Each Row** → Loops through data and calculates vendor totals  
6. 📈 **Excel Report Generation** → Monthly summary report created  
7. 📦 **File Handling** →  
   - ✅ Move valid invoices to *Archive*  
   - ⚠️ Move invalid/unreadable invoices to *Error*  
8. 📝 **Logging** → Errors written to *Records_Error.xlsx*  

---

---

## 📊 Output Files  
- **Records.xlsx** → All valid invoice entries  
- **Records_Error.xlsx** → Errors & failed extractions  
- **Monthly_Summary.xlsx** → Vendor-wise monthly totals  

*(Sample Excel outputs and sample invoices are included in this repo.)*  

---

## ⚙️ Tech Stack & Activities Used  
- **UiPath Studio** 🤖  
- **Activities Used:**  
  - Read PDF Text / Read PDF with OCR  
  - Matches (Regex)  
  - If / Assign (Validation Logic)  
  - Excel Write Range / Append Range  
  - For Each Row (Vendor totals)  
  - Move File (Archiving & Error handling)  
  - Try Catch (Exception handling)  

---

## 🚀 Impact  
- ⏳ Reduced processing time from **hours → minutes**  
- ✅ Improved **accuracy** and reduced manual errors  
- 📊 Automated vendor-wise monthly reporting (without PivotTables, using loops)  
- 🔄 Built a **scalable, reusable, and efficient bot**  

---

## 🌟 Key Learnings  
- Hands-on with **OCR & Regex** for text extraction  
- Applied **For Each Row** for reporting logic  
- Learned **validation & exception handling** in UiPath  
- Understood how **automation transforms finance workflows**  

---

## ▶️ How to Run This Project  
1. Clone this repository to your system.
```bash
git clone https://github.com/your-username/pdf-invoice-automation.git
```
2. Place sample invoice PDFs inside the **Input** folder.  
3. Open `Main.xaml` in **UiPath Studio**.  
4. Ensure the following dependencies are installed:  
   - UiPath.Excel.Activities  
   - UiPath.System.Activities  
   - UiPath.PDF.Activities  
   - UiPath.UIAutomation.Activities
   - UiPath.OCR.Activities
5. Run the workflow.  
6. Check Excel outputs in the repo.  

---
