# Language Detection NLP Project

## Overview
This project is designed to detect the language used by companies in their web presence. Utilizing a combination of web scraping techniques and NLP (Natural Language Processing), this project automates the process of identifying the primary language in which a company communicates on their official website.

## Workflow
The process involves several steps, illustrated in the provided workflow diagram:
1. **Web Scraping**: Automated scraping of content from company websites.
2. **Parsing HTML**: Using the BeautifulSoup library to parse the HTML content.
3. **Language Detection**: Employing a language detection algorithm or model to identify the language used in the scraped content.
4. **Data Storage**: Storing the company names and detected languages in a database.
5. **Comparison**: Comparing the detected language with the official language(s) of the company's country of operation.

## Components
- **Site Web**: The source of the company's web content.
- **Beautiful Soup**: A Python library for pulling data out of HTML and XML files.
- **Language Detector**: A component that detects the language from the text data.
- **Lingua Model**: An NLP model that is used for detecting the language.
- **Database**: A system for storing company names and detected languages.
- **Country_language**: The official language(s) of the company's country.
- **Name_language**: The language detected from the company's website.

## Output
The final output is a boolean value indicating whether the language detected (`Name_language`) matches any of the official languages of the country in which the company operates (`Country_language`).

## Usage
To use this project, follow these steps:
1. Ensure you have the necessary dependencies installed, including BeautifulSoup and any libraries required for the Lingua model.
2. Run the web scraping script to collect data from the targeted websites.
3. Parse the scraped data using BeautifulSoup to extract the relevant text.
4. Use the Language Detector with the Lingua model to determine the language of the extracted text.
5. Store the results in the Database with the new columns `Name_company` and `Name_language`.
6. Execute a comparison between `Name_language` and `Country_language` to check for a match.
7. The script will return `TRUE` if there's a match, or `FALSE` otherwise.
