# Amazon Product Scraper (UiPath)

This UiPath automation project is developed to efficiently extract structured product information from [Amazon.in](https://www.amazon.in) using browser automation and data scraping techniques. The process initiates a keyword-based product search (e.g., *"iPhone"*) and retrieves key data points including product name, price, rating, and availability.

The scraped data is programmatically exported to a formatted Excel spreadsheet, enabling seamless data analysis, market research, price comparison, and competitive tracking. This solution is particularly useful for e-commerce analysts, product managers, and automation developers looking to simplify web data extraction workflows.

---

## ⚙️ System Requirements

To run this project successfully, ensure your system meets the following requirements:

- **UiPath Studio** (tested with version `25.0+`)
- **Google Chrome** or **Microsoft Edge** with UiPath browser extension enabled
- Stable internet connection
- Excel-compatible environment (MS Excel not mandatory)

---

## 📦 Dependencies

All required packages are listed in the `project.json` file and are auto-restored when opened in UiPath Studio.

- `UiPath.Excel.Activities` `v3.0.1`
- `UiPath.System.Activities` `v25.4.4`
- `UiPath.UIAutomation.Activities` `v25.10.4`

Manage these packages via **Manage Packages** in UiPath Studio under *All Dependencies*.

---

## 🧩 Key UiPath Activities & Workflow Design

The automation leverages several foundational UiPath activities arranged in a clean and modular sequence. The main components of the workflow are as follows:

### 🔧 Activities Used

- **Sequence**: The base container to structure the logic step-by-step.
- **Use Application/Browser**: Automates interactions within the Amazon webpage using Chrome.
- **Delay**: Introduced between major steps to ensure page elements load completely.
- **Type Into**: Simulates keyboard input into Amazon's search bar based on data from Excel.
- **Extract Data Table**: Used for structured extraction of product details (name, price, ratings).
- **Write Range Workbook**: Writes the extracted data back into `iphonelist.xlsx` in `Sheet1`.

### 💡 Highlights

- All selectors are optimized for dynamic content.
- Delay and verification options are used to handle asynchronous page loading.
- Data table is extracted using UiPath’s Table Extraction Wizard for ease and accuracy.
- Excel interactions are performed using **Workbook activities**, removing the dependency on having Excel installed.

---

## 💡 Use Cases

- E-commerce product and pricing research
- Competitor tracking and benchmarking
- Automation of repetitive data collection tasks
- Academic projects or proof-of-concept automation workflows

---


## 🙌 Acknowledgements

Developed using **UiPath Studio**, leveraging its low-code RPA capabilities for efficient browser automation and Excel integration.
