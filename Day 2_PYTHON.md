## 🔹 1. Scraping

Scraping is the process of automatically extracting data from websites. It simulates how a user would browse a website but collects and stores data for analysis or automation. If a website allows scraping, we can use tools like BeautifulSoup or Selenium to pull that data. This is useful when there's no official API.

Example:

    When you want to collect product prices from an e-commerce site automatically.
  
  Legal/Ethical Note:
  
    Always check the website's robots.txt or terms of service.

  ## 🔹 Front End:
  
  What users interact with: HTML, CSS, JS.
  
  Tools like Chatbots, LLMs may use scraped data for responses.
  
  ## 🔹 Back End:
  
  The part where scraping is done using code and tools.
  
  Sends HTTP requests and parses responses.

## 🧰 2. Python Libraries for Scraping

## ✅ BeautifulSoup

    Used to parse static HTML content.
    
    Easy and lightweight.

Example:


        from bs4 import BeautifulSoup
        import requests
        
        url = "https://example.com"
        res = requests.get(url)
        soup = BeautifulSoup(res.text, 'html.parser')
        print(soup.title.text)
        
## ✅ Selenium

Used for dynamic content (JavaScript-based pages).

Automates browsers (Chrome, Firefox).

Example:

        from selenium import webdriver
        driver = webdriver.Chrome()
        driver.get("https://example.com")
        print(driver.title)
