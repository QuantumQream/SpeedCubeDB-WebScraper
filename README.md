# SpeedCubeDB-WebScraper
**WHAT IS THIS?**

This is a simple web scraping script I created to extract information about the 3x3 CFOP sub7 solves from SpeedCubeDB.
The script utilizes BeautifulSoup4 and common html tags to locate useful information on the solve's page
The script first grabs all the 'solve-ids' from the search page filtered to my desired conditions (3x3, CFOP and sub7) and then goes on to scrape the data from each one
The scraped data is then put into a pandas DataFrame and saved locally as a csv file

The goal of this project is to put my skills to the test in order to first adquire data and then put in a form that is easy to manipulate using basic DataScience techniques
After the data has been gathered I made a quite simple Exploratory Data Analysis (EDA) to produce cute graphs and diagrams that may shed some light on how the fastests cubers in the world approach their solves



**WHAT CAN BE DONE FROM HERE?**

- In a future revision I wish to re-write this code to introduce a class where each function can be a method that gets applied to objects (urls maybe?)
  I believe this will greatly improve the structure of the code and make it simple to expand in the future
  
- I wish to also include more feautures such as obtaining the specific cases for each step of the solve, this includes F2L, OLL, PLL, ZBLL, WV, COLL, etc...
  However this is not so simple as many times these cases are not fully written in the solve's page, it would be necessary to construct a way to identify a case given an algorithm

- Create more data visualizations in general

- Improve the web scraping script to make **EXTRA** sure it's a safe way to extract data without causing harm to SpeedCubeDB.
  I already implemented the sleep library to give some downtime between iterations, but I suspect more can be done
  

**KNOWN BUGS**

- The script stops at 1000 urls, I suspect I encountered a barrier by SpeedCubeDB to protect itself from persistent requests

- There are instances of some differently named/formatted html tags that don't follow the established pattern baked into my script
  Some notable instances are when the first step of the solve appears as 'nspection' (Which happened twice, I believe)
