# The Security Event (UK) Exhibitor Scraper

This project scrapes exhibitor information from **The Security Event (UK)** website, extracting exhibitor names and stand numbers from the public exhibitor list page. The script uses Python with `requests` and `BeautifulSoup` to parse static HTML content and generate a structured CSV file.

## Project Overview
The goal of this scraper is to quickly collect exhibitor data from a static, server-rendered page without needing a browser automation tool. The script fetches the exhibitor list, parses the HTML, extracts relevant information, and exports it into a clean CSV for further use.

## Features
- Sends HTTP requests to retrieve the exhibitor listing page  
- Parses exhibitor entries using BeautifulSoup  
- Extracts:
  - Exhibitor name  
  - Stand number (when available)  
- Saves results into `The Security Event_UK.csv`

## Tech Stack
- **Python**
- **Requests** for retrieving page content  
- **BeautifulSoup (bs4)** for HTML parsing  
- **CSV module** for structured output  

## How It Works
1. Send a GET request to the exhibitor listing page  
2. Parse HTML content using BeautifulSoup  
3. Locate all exhibitor list items (`li` elements)  
4. Extract:
   - `<h2>` — exhibitor name  
   - Stand meta tag — parsed from text (or fallback value if missing)  
5. Write the extracted data to a CSV file

## Output File
- **The Security Event_UK.csv**  
  Contains two columns:  
  - `Exhibitor`  
  - `Stand`  

## Use Cases
- Event research and planning  
- Competitor or market landscaping  
- Lead generation and contact mapping  
- Dataset preparation for business analytics  

## Notes
- This scraper works only because the page is **static HTML**.  
- If the website becomes JavaScript-rendered in the future, Selenium may be required.  
- Always review and respect the website’s terms of service before scraping.  
