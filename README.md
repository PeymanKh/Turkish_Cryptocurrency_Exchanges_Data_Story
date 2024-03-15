# Extracting and Visualizing the Dynamics of Leading Cryptocurrency Exchanges in Turkey

<img title="a title" alt="Alt text" src="https://www.cpapracticeadvisor.com/wp-content/uploads/sites/2/2022/07/30017/big_data_1_.5afaec15da23c.png">

## Table of Contents
- [1. Web Scraping](#WebScraping)
- [2. Scrapy Library](#Scrapy)
- [2. Files Overview & Execution Instructions](#Repository)
- [2. Data Source](#References)

References

<a name="WebScraping"></a>
## 1. Web Scraping
Web scraping, also known as web data extraction, is the process of retrieving or “scraping” data from websites. This technique is used to convert the data available on websites into a structured format that can be stored and analyzed. Web scraping is widely used in various industries for different purposes, such as price monitoring, market research, lead generation, and competitive analysis.

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

Extracting data using Scrapy library is done by "spiders", which are classes in Scrapy that detail how to perform the scraping. Spiders include the initial URLs to scrape, how to follow links, and how to parse the downloaded page content to extract data. To create a project and setup a spider you can use following commands on your IDE's terminal:
```sh
scrapy startproject projectName
```
```sh
scrapy genspider spiderName URL
```

After initializing your project using above commands, You can see your project's spider.py in the following format:

```python
import scrapy

class ExampleSpider(scrapy.Spider):
    name = 'example'
    allowed_domains = ['example.com']
    start_urls = ['http://example.com/']
    
    def parse(self, response):
        # Your parsing code here
```

After finalizing your spider.py parse function, You can crawl the target web page to extract the desired data points using the folloing commad:
```sh
scrapy crawl spiderName -O fileName.json/fileName.CSV
```


<a name="Repository"></a>
## 3. Files Overview & Execution Instructions
This Project consists of 3 folders:

1. ***WebScraping***: This directory houses the Scrapy project. The data_scraper.py file within the spiders folder is crafted to gather real-time data from leading Turkish cryptocurrency exchanges, utilizing bitdegree.org—a website renowned for its cryptocurrency-related information. The scraping operation was carried out on March 14, 2024, at 13:00 (GMT+3). To run the data extraction process on your machine, download this folder, navigate to `1- WebScraping/bitdegree/spiders` via terminal using bash commands, and execute `scrapy crawl data_scraper -O data.json.` Upon completion, the extracted data will be stored in `/spiders/data.json`.

2. ***Data Cleaning & Visualization***:
After extracting the data, we copy data.json to the Data Cleaning & Visualization folder for further cleaning and analysis. The DataProcessing.ipynb Jupyter Notebook contains steps for processing the data and creating visualizations with pandas, matplotlib, and seaborn libraries, helping us to better understand our data.

2. ***The Story Behind The Data***: This folder includes the ultimate visualization of our data in Data Story.pdf. It provides valuable insights into the status of leading cryptocurrency exchanges, market trends, website metrics, and more, aiding in making informed decisions. You can Downalod the final PDF file [here](https://github.com/PeymanKh/Turkish_Cryptocurrency_Exchanges_Data_Analysis/files/14620025/Data.Story.pdf).

<a name="References"></a>
## Data Source:
- https://www.bitdegree.org


