Here’s a README for your project:

---

# Invoice PDF Generator

This project is a Python script that automates the generation of PDF invoices from Excel files. Using data from `.xlsx` files in a specified directory, the script creates a professional-looking PDF invoice for each file. It utilizes `pandas` to read data, `FPDF` to generate PDFs, and `pathlib` and `glob` for file path management.

## Features

- Reads data from multiple `.xlsx` files in the `invoices` folder.
- Generates a PDF invoice for each file, saving them in the `PDFs` folder.
- Extracts invoice number and date from the filename for easy reference.
- Dynamically creates tables for each invoice’s line items.
- Displays total amount with a final summary line.
- Adds company name and logo to each PDF.

## Prerequisites

- Python 3.x
- Required libraries:
  - `pandas`
  - `fpdf`
  - `glob`
  - `pathlib`

You can install the necessary libraries with:
```bash
pip install pandas fpdf
```

## Folder Structure

Ensure that your directory structure looks like this:
```
project-folder/
├── invoices/
│   ├── invoice1-2023-10-01.xlsx
│   └── invoice2-2023-10-02.xlsx
├── PDFs/
│   └── (generated PDFs will be saved here)
├── pythonhow.png
└── main.py (this script)
```

## Usage

1. Place your `.xlsx` invoice files in the `invoices/` folder. Each filename should follow the format `invoice_number-date.xlsx`, e.g., `invoice1-2023-10-01.xlsx`.
2. Run the script:
   ```bash
   python main.py
   ```
3. Generated PDF files will be available in the `PDFs` directory.

## Example File Format

Each `.xlsx` invoice file should contain a sheet named "Sheet 1" with the following columns:

| product_id | product_name   | amount_purchased | price_per_unit | total_price |
|------------|----------------|------------------|----------------|-------------|
| 001        | Product A      | 10               | 5             | 50          |
| 002        | Product B      | 5                | 10            | 50          |

## Code Explanation

The script:
- **Reads each Excel file** using `pandas`, identifying invoice numbers and dates from filenames.
- **Creates a PDF** with FPDF, setting up page orientation, font, and layout.
- **Generates a table** for line items and calculates the total amount.
- **Adds a summary** of the total sum for each invoice at the bottom.
- **Embeds company details** like name and logo.

## License

This project is open-source and freely available for modifications and enhancements.

--- 

This README should provide clear instructions for setup and usage. Let me know if you'd like further customization!