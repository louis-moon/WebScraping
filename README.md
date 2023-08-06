# Web Scraper for School Profiles

## Overview
For the nonprofit startup Equity A1, this repository contains code to scrape public high school profiles from Niche.com. Data points include school names, state, zip code, number of students, and household income. Additionally, the tool sorts and filters the schools based on student count and organizes the information in a binary tree for efficient access.

## Features
- Web Scraping: Uses BeautifulSoup and scraperapi.com to efficiently parse HTML content from Niche.com and extract relevant school data.

- Concurrency: Employs multi-threading through concurrent.futures for speedy data extraction across multiple pages.

- Binary Tree Organization: The data is not only scraped but also organized into a balanced binary tree for efficient access and queries based on student count.

- Data Filtering: With the findSchool function, you can easily filter out schools based on student count.

- CSV Export: The scraped data is exported to a CSV file for further analysis or reporting.

## Modules
1. Node Class & Binary Tree Building:

- A tree node holds the school's data.
- The binary tree is constructed using a recursive algorithm.
2. Data Scraping:

- Functions extract raw content from URLs, convert it into BeautifulSoup objects, and then extract the desired data, such as school profiles.
School Finding & Data Export:

- findSchool: A recursive function to find and list schools based on a student count threshold.
- Data, once scraped, is written to a CSV file using Python's built-in CSV module.
## Constants
- API_KEY: Your scraperapi.com API key.
- NUM_RETRIES: Number of retries for each URL request.
- NUM_THREADS: Number of threads used in the scraping process.
- page_beg: Base URL for initiating the scrape.
## Dependencies
- BeautifulSoup
- requests
- concurrent.futures
- csv
- urllib
- pandas
- time
## Usage
1. Install required dependencies.
2. Update constants as necessary, particularly the API_KEY.
3. Run the script to start the scraping process.
4. The extracted data will be saved in test.csv and can be further used for analysis or reporting.
## Future Improvements
1. Enhance scraping capabilities to cover more data points or different websites.
2. Implement a more comprehensive storage system like a database.
3. Boost error handling and edge-case management for robust scraping.
