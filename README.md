# Excel to PDF Invoice Generator

This Python script converts Excel-based invoices into **professional PDF invoices** using `pandas` and `FPDF`. It reads all Excel files in a folder, extracts invoice details, and generates formatted PDF invoices automatically.

---

## Features

- Automatically reads multiple Excel invoice files from a folder.
- Extracts invoice number, date, and product details.
- Generates PDF invoices with:
  - Invoice number and date at the top
  - Tabular format for products (ID, Name, Quantity, Price, Total)
  - Total amount due
  - Custom branding (logo/image)
- Saves PDFs in a separate output folder (`Invoices_Docs`).

---

## Requirements

- Python 3.x
- Packages:
  - `pandas`
  - `fpdf`
  - `pathlib`
  - `glob`

Install dependencies using pip:

```bash
pip install pandas fpdf pathlib
