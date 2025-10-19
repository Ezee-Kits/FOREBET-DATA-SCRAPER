# FOREBET-DATA-SCRAPER
Automates scraping of daily football predictions from Forebet (1X2, Over/Under 2.5, Both Teams To Score) with Pyppeteer and BeautifulSoup. Scrolls pages and clicks "MORE" to load matches, parses match date/time and team stats, merges three datasets into a cleaned pandas DataFrame, deduplicates, and saves a daily CSV.
