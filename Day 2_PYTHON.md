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

## 3. Virtual Environment & Poetry

## 🔹 Why Virtual Environments?

Keeps your project’s dependencies separate from global Python packages.

Prevents version conflicts.

## 🔹 Using venv (basic way):

        python -m venv env
        source env/bin/activate  # or env\Scripts\activate on Windows
        
## 🔹 Using Poetry (modern way):

Automatically handles dependency versions and virtual environments.

        pip install poetry
        poetry init  # creates pyproject.toml
        poetry add beautifulsoup4 selenium
        poetry shell  # activates the environment

## ✅ 4. Probability (Basic Idea)

Probability is the measure of how likely an event is to happen.

It ranges from 0 to 1 (or 0% to 100%).

        Example: The probability of flipping a coin and getting heads = 0.5.

## ✅ Conditional Probability

This is the probability of an event happening given that another event has already occurred.

            Formula:
    
            P(A∣B)= P(A∩B)/ P(B)
​
        Example:
        
        A bag has 3 red and 2 blue balls.
        
        If you know a ball is not blue, what's the chance it's red?
        
        Given it's not blue (so only red balls left), the chance it's red is 100%.

## ✅ Expected Value (Expectation)

The average result if you repeat a random process many times.

            E(X)=∑(xi⋅P(xi))
        
        Example:
        
        Rolling a fair die:
        
        E=(1+2+3+4+5+6)/6=3.5
        
## ✅ 4. Mean

The mean is just the average of numbers.

        Formula:
        Mean= (x1+x2+⋯+xn)/n
​
        Example:
        
        Numbers: 2, 4, 6 → Mean = (2+4+6)/3 = 4

## ✅ 5. Variance

Variance measures how much values are spread out around the mean.

        Formula:
        
        Variance= n∑(xi−μ)2/n
 
        Example:
        
        If values are all close to the mean, variance is small. If values vary a lot, variance is large.

## ✅ 6. Self-Explanatory

In your notes, self-explanatory likely refers to topics that are simple enough to understand on their own, like:

        Mean → everyone knows it’s an average.
        
        Expected value → just like taking average results.
        
        Probability → how likely something is to happen.
        
        These concepts are foundational and often used in:
        
        Surveys (like elections),
        
        Games (dice, cards),
        
        AI/ML models (prediction based on probability).


