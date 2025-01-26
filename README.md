# Website Data Scraper

A powerful Python-based web scraper that extracts text, images, and videos from websites. The scraper features advanced options for data processing, including keyword filtering, text extraction from images, and multi-format data export.

## Features

- Scrape text, images, and videos from websites.
- Extract text from images using Tesseract OCR.
- Keyword-based content filtering.
- Multi-format data saving: JSON, TXT, DOCX, CSV, PDF, and XLSX.
- Real-time progress bar and time estimation for scraping tasks.
- User-friendly command-line interface with colorful output.

## Prerequisites

To use this scraper, ensure the following dependencies are installed:

- Python 3.8 or higher
- Selenium
- BeautifulSoup4
- PyTesseract
- Pillow
- Python-Docx
- PyFiglet
- Colorama
- FPDF
- Pandas

You can install the dependencies using the following command:

```bash
pip install selenium beautifulsoup4 pytesseract pillow python-docx pyfiglet colorama fpdf pandas
```
# Installation
1. Clone the repository or copy the script to your local machine.
2. Install the dependencies as listed above.
3. Ensure you have Tesseract OCR installed and added to your system's PATH. [Download it here](https://github.com/tesseract-ocr/tesseract).

---

# Usage
Run the script:

```bash
python scraper.py
```
# Enter the Required Inputs as Prompted

- **Website URL**: Provide the URL of the website to scrape.
- **Keyword**: Specify a keyword to filter content (leave empty to scrape all content).
- **Folder Name**: Define a folder to save results.
- **File Format**: Choose a format for saving data (e.g., `json`, `txt`, `docx`, `csv`, `pdf`, `xlsx`).
- **Scrape Images**: Choose whether to scrape images (`yes/no`).
- **Scrape Videos**: Choose whether to scrape videos (`yes/no`).
- **Extract Text from Images**: Specify if text should be extracted from images (`yes/no`).
- **Scrape Specific Page**: Optionally scrape a specific page.
- **Scrape All Pages**: Choose to scrape the entire site (`yes/no`).

The scraper will process the website and save the results in the specified folder and format.

---

# Key Functions

### `create_results_folder(folder_name)`
Creates a folder for saving results if it doesn't already exist.

### `display_banner()`
Displays a banner showcasing the scraper's name and functionality.

### `spinner_animation()`
Shows a spinning animation while scraping is in progress.

### `detect_website_info(soup)`
Extracts basic website information using OG meta tags or the title.

### `extract_text_from_image(image_path)`
Uses Tesseract OCR to extract text from images.

### `download_image(driver, image_url, save_path)`
Downloads and saves an image from the website.

### `print_progress_bar(iteration, total, prefix='', suffix='', length=40, fill='█')`
Displays a real-time progress bar for scraping tasks.

### `scrape_page(...)`
Handles the scraping of a single page, including text, images, and videos.

### `save_data(data, folder_name, file_format, keyword=None)`
Saves scraped data in the specified format.

### `scrape_website()`
The main function that orchestrates the entire scraping process.

---

# Example Workflow

1. Launch the script.
2. Input a URL like `https://example.com`.
3. Specify if you want to scrape images, videos, or extract text from images.
4. Choose a file format, e.g., `json` or `csv`.
5. Let the scraper process the website. The results will be saved in the specified folder.

---

# Outputs

The scraper supports the following output formats:

- **JSON**: A structured format for developers.
- **TXT**: Plain text format for readability.
- **DOCX**: A Microsoft Word file.
- **CSV**: Tabular data for spreadsheets.
- **PDF**: Printable format.
- **XLSX**: Excel spreadsheet for advanced data handling.

---

# Notes

- **Tesseract OCR**: Ensure Tesseract is installed and accessible via your system's PATH for text extraction from images.
- **WebDriver**: Install the appropriate WebDriver (e.g., ChromeDriver) compatible with your browser version.
- **Performance**: Large websites or extensive scraping tasks may take time. Use the progress bar and estimated time feature for monitoring.

---

# Acknowledgements

Script written by **Dev Elijah**.

---

# License

This script is provided "as is" without any warranties. Use it responsibly and ensure compliance with website terms of service.
