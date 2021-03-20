# Partner Power Hour #1 - 3/20/2021 
**Presenter: Chance Harmon**    
**Topic: Intro to Web Scraping with Node.JS and Puppeteer**   

Chance Harmon is code fellows graudate and he was talking about the web scraping. He used JS library Puppeteer with Node.JS to demonstrate the web scraping.    

1. Install the puppeteer    
    `npm i puppeteer`

2. Demo code  
    ```JavaScript
    // import the puppeteer
    const puppeteer = require('puppeteer');

    (async () => {
      let browser = await puppeteer.launch();
      
      let page = await browser.newPage();

      page.setUserAgent(<'google your user agent and past it here'>);

      let url = 'https://www.codefellows.org';

      await page.goto(url, { waitUntil: 'networkidle2' });

      // Scraping for single content
      let singleContent = await page.evaluate(() => {
        // target content template: document.querySelector(...)
        return <'target content'>;
      });
      console.log(singleContent);

      // Scraping for multiple content and store it in an array
      let stats = await page.evaluate(() => {
        return Array.from(<'target contet'>, element => element.textContent);
      })
      console.log(stats);

      await browser.close();
    })();
    ```

3. [Puppeteer Official Docs](https://www.npmjs.com/package/puppeteer)