Krakow Real Estate Market Analysis (OLX Scraper)
Project Description
An automated system for acquiring and analyzing apartment price data in Krakow. The project covers the full ETL (Extract, Transform, Load) pipeline: from scraping data from the OLX portal, through validation and cleaning in Python, to storage in a PostgreSQL relational database and final visualization in Power BI.

Technologies Used
Python 3.x (Requests, BeautifulSoup4, Pandas, Re)

PostgreSQL

Power BI

Git

Solution Architecture
Data Extraction: The scraper.py script retrieves data from multiple pages, bypassing dynamic HTML structure changes by utilizing text pattern matching.

Data Cleaning: Regular expressions (Regex) are used to extract floor area and district names, as well as to clean price strings from incorrect formatting and units.

Data Storage: Data is exported to a PostgreSQL database to ensure data consistency and enable advanced SQL analysis.

Visualization: An interactive Power BI report allowing for price filtering by district and identification of market outliers (investment opportunities).

Repository Structure
/scraper.py - Parser source code.

/schema.sql - Database table definition.

/requirements.txt - Python dependency list.

/data_sample.csv - Exported sample data.
