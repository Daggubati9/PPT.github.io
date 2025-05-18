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

## 📊 What is a Distribution?

A probability distribution is a statistical function that describes all the possible values and likelihoods that a random variable can take within a given range.

    A distribution shows how data values are spread.
    
    Helps in understanding the probability of outcomes.
    
    Common in data science, machine learning, and statistics.


## ⭐ Bernoulli Distribution

A Bernoulli distribution is a discrete probability distribution for a random variable which takes the value 1 with probability p and the value 0 with probability 1-p.

    Only two outcomes: Success (1) or Failure (0)

    One trial only (e.g., tossing a coin)
    
    Formula: P(X=1) = p, P(X=0) = 1-p
    
    Example: Did a user click the button? Yes = 1, No = 0

## ✔️ Binomial Distribution

A binomial distribution summarizes the likelihood that a value will take one of two independent values under a given set of parameters or assumptions.

    Multiple independent Bernoulli trials
    
    Answers: How many successes in n trials?
    
    Formula: P(X = k) = C(n, k) * p^k * (1-p)^(n-k)
    
    Example: Out of 10 exams, how many did you pass?

## ⚙️ Data Preparation Steps

Data preparation is the process of cleaning and transforming raw data prior to processing and analysis. It's an essential step for accurate results in data science.

Step 1: Understand (Under)

    Know your dataset (binary/categorical/numeric)

Step 2: Clean

    Handle missing values
    
    Encode values (e.g., Yes/No -> 1/0)

Step 3: Prepare

    Format data for analysis

Define probabilities and count of trials

## 📈 Types of Distributions

| **Distribution** | **Description**                       | **Example**                           |
| ---------------- | ------------------------------------- | ------------------------------------- |
| **Bernoulli**    | One trial with two outcomes (0 or 1)  | Tossing a coin (Heads = 1, Tails = 0) |
| **Binomial**     | Repeated Bernoulli trials             | Passing 7 out of 10 quizzes           |
| **Normal**       | Bell-shaped curve for continuous data | Heights of students in a class        |
| **Poisson**      | Counts events in a fixed interval     | Calls received per minute             |
| **Uniform**      | All outcomes equally likely           | Rolling a fair six-sided die          |
| **Exponential**  | Time between independent events       | Time between bus arrivals             |

Example:

        from scipy.stats import bernoulli, binom
        
        print(bernoulli.pmf(1, 0.7))     # Output: 0.7
        print(binom.pmf(5, 10, 0.5))     # 5 successes in 10 trials

## ✅ Distribution of X

A distribution shows how the values of a random variable 𝑋. X are spread — or how likely each value is."

    Example:
    Rolling a 6-sided die.
    X = 1, 2, 3, 4, 5, 6
    P(X) = 1/6 for each value
    
## ✅ Expectation (Expected Value)

Expectation is the average value we expect after many repetitions of a random process.

    Formula: E[X]=∑xi⋅P(xi)

    Example:
        Rolling a fair die:
        
        𝐸
        [
        𝑋
        ]
        =
        1
        ⋅
        1
        6
        +
        2
        ⋅
        1
        6
        +
        ⋯
        +
        6
        ⋅
        1
        6
        =
        3.5
        E[X]=1⋅ 
        6
        1
        ​
         +2⋅ 
        6
        1
        ​
         +⋯+6⋅ 
        6
        1
        ​
         =3.5
