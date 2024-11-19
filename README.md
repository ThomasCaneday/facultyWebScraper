# University Faculty Directory Scraper

## Description
This Python script is designed to scrape faculty contact information from university directories. It specifically searches for and extracts information about key administrative roles such as Provost, CIO, and Dean of Learning Technologies.

## Features
- Web scraping of faculty directories
- Filtering for specific administrative roles
- Extraction of contact details including:
  - Name
  - Title
  - Email address

## Requirements
- Python 3
- Required packages:
  - `requests`
  - `beautifulsoup4`

## Installation
1. Install the required packages:
```bash
pip install requests beautifulsoup4
```

## Usage
1. Run the script:
```bash
python search_faculty.py
```
2. When prompted:
   - Enter the university name
   - Provide the URL of the faculty directory

## How it Works
1. The script takes two inputs:
   - University name
   - Faculty directory URL
2. It sends an HTTP request to the provided URL
3. Parses the HTML content using BeautifulSoup
4. Searches for contact information in `div` elements with class `contact-info`
5. Filters results for specific roles:
   - Provost
   - CIO
   - Dean of Learning Technologies
6. Displays the filtered results including name, title, and email

## Example Output
```
Name: John Doe, Title: Provost, Email: john.doe@university.edu
Name: Jane Smith, Title: CIO, Email: jane.smith@university.edu
```

## Notes
- The script assumes a specific HTML structure with classes:
  - `contact-info` for contact containers
  - `title` for job titles
  - `email` for email addresses
- You may need to modify the HTML selectors based on the specific structure of your target website
- Ensure you have permission to scrape the target website
- Respect the website's robots.txt and terms of service

## Legal Considerations
- Always check and comply with the website's terms of service
- Respect rate limits and robots.txt
- Be mindful of data privacy regulations
