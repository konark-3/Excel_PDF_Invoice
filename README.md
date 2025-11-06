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

`pip install pandas fpdf pathlib`

## ⚙️ Setup

1\. Place all invoice `.xlsx` files inside an `Invoices/` folder.  

Each file should be named in the format:  

<InvoiceNumber>-<Date>.xlsx

Example:  

`1001-2025-11-06.xlsx`

2\. Install dependencies:


`pip install pandas fpdf`

- Add a company logo image named pythonhow.png in the project root.

- Create a folder named Invoices_Docs/ --- generated PDFs will be saved there.

## 🚀 How It Works

- Reads all Excel files from the Invoices/ folder.

- Extracts invoice number and date from the filename.

- Reads item data (product name, quantity, price, etc.) using pandas.

- Builds a clean PDF invoice layout using FPDF:

- Adds invoice details

- Displays items in a table

- Calculates and shows total amount

- Adds a footer with branding and logo

- Saves each invoice as a .pdf file in Invoices_Docs/.

## 💡 Example Usage

Run the script:

`python invoice_to_pdf.py`

Output:

`Invoices_Docs/1001-2025-11-06.pdf`

Each PDF will include:

- Invoice number and date

- Itemized product table

- Total price summary

- Company footer and logo

## 📝 Notes

- Ensure column names in Excel match:

- product_id, product_name, amount_purchased, price_per_unit, total_price

- The logo image path can be updated in the script if needed.

- The script automatically calculates and formats totals for each invoice.
