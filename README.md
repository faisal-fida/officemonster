# Officemonster

This project is a comprehensive web scraping application designed to collect product data from a specified e-commerce website. The project consists of two main Jupyter notebooks: `URLS Scraper.ipynb` and `Product Scraper.ipynb`.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Complexities](#complexities)
- [Solutions](#solutions)
- [Challenges](#challenges)
- [License](#license)

## Installation

1. Clone the repository:

```sh
git clone https://github.com/faisal-fida/officemonster.git
cd officemonster
```

2. Install the dependencies:

```sh
pip install -r requirements.txt
```

3. Make sure you have the required CSV files in the `URLS` directory.

## Usage

### URLS Scraper

1. Open `URLS Scraper.ipynb` to run the script that processes multiple CSV files in the `URLS` directory, concatenates them, and saves the combined URLs to `combined_urls.csv`.
2. The script then extracts URLs from `combined_urls.csv` and saves them to `urls.csv`.

### Product Scraper

1. Open `Product Scraper.ipynb` to run the script that reads URLs from `urls.csv` and scrapes product details.
2. The script utilizes BeautifulSoup to parse HTML content and extract relevant product information such as title, price, images, and descriptions.

## Features

- **Data Aggregation**: Combining multiple CSV files into a single DataFrame while maintaining data integrity.
- **Web Scraping**: Handling dynamic web content and possible changes in website structure.
- **Error Handling**: Managing HTTP errors and ensuring the script continues to run smoothly.

- **Efficient Data Handling**: Used `pandas` to efficiently read, concatenate, and save CSV files.
- **Robust Web Scraping**: Implemented functions to handle HTTP requests and parse HTML with BeautifulSoup, ensuring data is extracted even if some pages do not follow the expected structure.
- **Error Management**: Added try-except blocks to catch and log HTTP errors, allowing the script to skip problematic URLs and continue processing others.

- **Data Consistency**: Ensuring all CSV files have a consistent format and contain valid URLs.
- **Website Variability**: Handling variations in web page design that could affect scraping logic.
- **Performance**: Optimizing the script to handle large datasets and multiple HTTP requests efficiently.
