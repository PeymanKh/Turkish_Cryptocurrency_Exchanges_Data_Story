# Analyzing and Visualizing the Dynamics of Leading Cryptocurrency Exchanges in Turkey

## Table of Contents
- [1. Web Scraping](#WebScraping)
- [2. Scrapy Library](#Scrapy)



<a name="WebScraping"></a>
## 1. Web Scraping
Web scraping, also known as web data extraction, is the process of retrieving or “scraping” data from websites. This technique is used to convert the data available on websites into a structured format that can be stored and analyzed. Web scraping is widely used in various industries for different purposes, such as price monitoring, market research, lead generation, and competitive analysis. Here's a breakdown of the key aspects of web scraping:

## How Web Scraping Works:
1. **Requesting Data**: The first step involves sending a request to the website’s server to retrieve the webpage. This is usually done using HTTP or HTTPS protocols.
2. **Parsing Data**: Once the webpage is retrieved, the next step is to parse the HTML or XML content of the page to extract the specific data you need. This is typically achieved using scraping libraries.
3. **Extracting Data**: After parsing the webpage, the desired data can be extracted using various selectors like XPath, CSS selectors, or regular expressions. The extracted data might include text, links, images, and more.
4. **Storing Data**: The extracted data is then stored in a structured format such as CSV, JSON, or a database. This allows for easier access and analysis of the data.


<a name="Scrapy"></a>
## 2. Scrapy Library
Scrapy is a fast, high-level web crawling and web scraping framework, widely used for extracting the data from websites. It is written in Python and provides a simple, yet powerful, interface for crawling websites and extracting structured data. Scrapy is designed with extensibility in mind, allowing developers to write reusable code for different scraping tasks. It's an open-source tool, which makes it freely available for modification and distribution, fostering a vibrant community of contributors. Scrapy operates by sending HTTP requests to websites, parsing the responses, and extracting data based on predefined selectors.

## Installing Scrapy:
```sh
pip install scrapy
```

Extracting data using Scrapy library is done by "spiders", which are classes in Scrapy that detail how to perform the scraping. Spiders include the initial URLs to scrape, how to follow links, and how to parse the downloaded page content to extract data. To create a project and setup a spider you can:
```sh
scrapy startproject projectName
```
```sh
scrapy genspider spiderName URL
```

After initializing your project using above codes, You can see the project's spider script in the following format:

```python
import scrapy

class ExampleSpider(scrapy.Spider):
    name = 'example'
    allowed_domains = ['example.com']
    start_urls = ['http://example.com/']
    
    def parse(self, response):
        # Your parsing code here
```









