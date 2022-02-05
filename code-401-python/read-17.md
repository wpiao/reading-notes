# Read: 17 - Web Scraping - 02/05/2022

Web scraping - a techinique to automatically access and extract large amounts of information from a website, which can save a huge amount of time and effort.

- Inspecting the website - locate the data you want to extract
- Python code example with `BeautifulSoup` library

  ```python
  import requests
  import urllib.request
  import time
  from bs4 import BeautifulSoup

  url = "http://web.mta.info/developers/turnstile.html" # This is the url that you want to scrape the data from

  response = requests.get(url)

  soup = BeautifulSoup(response.text, "html.parser")

  # loop through all "a" tags in soup
  line_count = 1 #variable to track what line you are on
  for one_a_tag in soup.findAll('a'):  #'a' tags are for links
      if line_count >= 36: #code for text files starts at line 36
          link = one_a_tag['href']
          download_url = 'http://web.mta.info/developers/'+ link
          urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
          time.sleep(1) #pause the code for a sec
      #add 1 for next line
      line_count +=1
  ```
