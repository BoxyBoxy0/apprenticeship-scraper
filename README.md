APPRENTICESHIP SCRAPER
=====================

This project is a Python script that scrapes apprenticeship listings from:
https://www.findapprenticeship.service.gov.uk

It exports results to a CSV file with properly parsed, sortable dates that
work correctly in Excel.

The script handles closing date formats such as:
- Closes in 25 days (Friday 6 March 2026)
- Closes in 19 days (Saturday 28 February 2026 at 11:59pm)

and converts them into real calendar dates (YYYY-MM-DD).


REQUIREMENTS
------------

- Windows
- Google Chrome installed


USAGE
-----

1. Go to:
   https://www.findapprenticeship.service.gov.uk

2. Search for apprenticeships using the website filters
   (location, keyword, level, distance, etc.)

3. Copy the resulting URL from your browser.
   This URL contains all the search parameters.

   Example:
   https://www.findapprenticeship.service.gov.uk/apprenticeshipsearch?
   Location=London&Distance=30&SearchTerm=engineering

4. Run the program:

5. Paste the full URL into the prompt after running it.

The script will automatically:
- Navigate through all result pages
- Extract apprenticeship data
- Save the output as a CSV file in the current directory


OUTPUT
------

The CSV file contains the following columns:

- title
- link
- distance_miles
- wage_gbp
- closing_date (YYYY-MM-DD)
- raw_text

Dates are stored in ISO format so they sort and filter correctly in Excel.


NOTES
-----

- If Excel shows ##### in the closing_date column, the data is still correct.
  Resize the column or set the date format to YYYY-MM-DD.


- To narrow down results, always refine the search on the website first,
  then copy the URL rather than modifying the script.


DISCLAIMER
----------

This project is intended for educational and personal use.
Always respect the website’s terms of service when scraping.


END
===
