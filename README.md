# Job Scraper Project

## Overview
This project is a browser automation and web scraping tool designed to extract job listings from a dynamically generated website. Using Splinter and browser-based navigation, the scraper systematically captures visible job information across multiple pages and compiles the results into a structured CSV file for analysis.

The tool demonstrates how to handle:
- Dynamic page loading
- Multi-page navigation (pagination)
- Element interaction (even with obstructive page elements)
- Data extraction into a clean tabular format

---

## Technologies Used
- **Python 3**
- **Splinter** (browser automation)
- **Selenium WebDriver** (underlying browser control)
- **Pandas** (data manipulation and CSV export)
- **ChromeDriver** (for interacting with Chrome browser)

---

## Features
- Automatically navigates through all pages of job listings.
- Captures all visible details per job (title, location, department, etc.).
- Handles dynamic content and page layout issues gracefully.
- Outputs a clean `.csv` file containing all extracted job data.

---

## Setup Instructions

1. **Install Required Packages**

```bash
pip install splinter selenium pandas
```

2. **Download ChromeDriver**
   - Ensure you have [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) installed and compatible with your Chrome version.
   - Place it somewhere accessible in your system PATH, or specify its path explicitly in the code.

3. **Run the Scraper**
   - Execute the script or notebook to start scraping job listings.
   - The output will be saved as a `.csv` file in the working directory.

---

## How It Works

- **Browser Launch**: The script launches a Chrome browser using Splinter.
- **First Page Scrape**: It scrapes all job listings from the initial page.
- **Pagination**: It detects and clicks the "Next" button, even if overlaid by other elements, using JavaScript-based clicks.
- **Data Storage**: Captured job details are stored in a Pandas DataFrame.
- **CSV Export**: Once scraping completes, the data is exported to a `.csv` file.

---

## Notes
- Make sure your Chrome browser version matches the ChromeDriver version.
- Ensure stable internet connection as the script interacts with a live website.
- Be mindful of website scraping policies (robots.txt and terms of service) when running the scraper at scale.

---

## Example Output

| Job Title | Location | Department | Posting Date | ... |
|:---|:---|:---|:---|:---|
| Data Analyst | Oakland, CA | IT | 2025-04-28 | ... |
| Project Manager | Pasadena, CA | Operations | 2025-04-27 | ... |

---

## Future Improvements
- Implement automatic ChromeDriver management (e.g., using `webdriver-manager`).
- Add error handling for session timeouts or unexpected site changes.
- Extend to scrape additional fields or filter job types dynamically.

---

## License
This project is for educational and demonstration purposes.