# spare-parts-reconciliation
Python script for automated part number reconciliation using OCR, PDF parsing, and Excel automation.

# 🛠️ Spare Part Match with OCR and Excel Automation

This project demonstrates how Python can be used to automate spare part tracking by extracting part numbers from scanned PDF manuals and updating a structured Excel file. It uses **OCR**, **fuzzy matching**, and **data validation** to identify known and superseded parts and enhance records with machine name tagging.
Open the [Colab notebook]https://colab.research.google.com/drive/1yVDm_NJnxwi-mBz9CuzxXCyFSQNwNOqJ?usp=sharing.

---

## 🚀 Key Features

- ✅ Extracts part numbers from both text-based and scanned PDFs using **PyMuPDF** and **Tesseract OCR**
- ✅ Normalizes and validates part numbers using **regex** and custom logic
- ✅ Matches extracted parts with an existing **Excel inventory sheet**
- ✅ Applies **fuzzy matching** (difflib) to find likely superseded parts
- ✅ Adds a machine name to relevant Excel entries and color-codes them
- ✅ Saves a clean, updated Excel file for reporting or re-upload

---

## 🧰 Technologies Used

| Tool/Library     | Purpose                         |
|------------------|----------------------------------|
| Python           | Core logic and scripting         |
| `fitz` (PyMuPDF) | Fast PDF text extraction         |
| `pytesseract`    | OCR for scanned documents        |
| `pdf2image`      | Convert PDFs to images for OCR   |
| `pandas`         | Data handling (minimal use)      |
| `openpyxl`       | Read/write Excel with formatting |
| `re`             | Regex for part number extraction |
| `difflib`        | Fuzzy matching for similar parts |

---

## 📊 Real-World Use Case

> Used in a manufacturing environment to:
> - Extract and match spare part numbers from equipment manuals.
> - Track replacements and superseded parts.
> - Automatically update Excel-based part registries with clear indicators for maintenance teams.

---

## 📁 File Overview

| File                            | Description                                      |
|---------------------------------|--------------------------------------------------|
| `Spare_Part_Match.ipynb`        | Main Colab notebook                              |
| `Updated_Spare_Parts.xlsx`      | Final output with machine names added            |
| (Optional) `manual_sample.pdf`  | Sample scanned equipment manual (for testing)    |

---

## ⚙️ How It Works

1. **Load** all PDF files in a directory (`/content/*.pdf`)
2. **Extract** part numbers from each using OCR + regex
3. **Normalize** both PDF and Excel part numbers
4. **Compare** extracted parts with Excel using exact and fuzzy matching
5. **Update** the Excel machine name column and highlight relevant entries
6. **Save** the results in a new file (`Updated_Spare_Parts.xlsx`)

---

## 🧠 Skills Demonstrated

- Data Extraction and Preprocessing
- Regex and Text Pattern Matching
- Optical Character Recognition (OCR)
- Fuzzy Matching with difflib
- Excel Automation (data + formatting)
- Real-world problem solving in inventory management

---

## 📌 Setup & Requirements

Install dependencies:

```bash
pip install pymupdf pytesseract pdf2image openpyxl pandas
 
