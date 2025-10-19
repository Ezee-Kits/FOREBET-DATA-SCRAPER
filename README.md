# Forebet Data Scraper

## 📖 Overview
**Forebet Data Scraper** is an automated Python script that extracts daily football prediction data from [Forebet.com](https://www.forebet.com/).  
It collects match predictions across three categories — **1X2 results**, **Over/Under 2.5 goals**, and **Both Teams to Score (BTS/OTS)** — and compiles them into a clean, well-organized CSV file for daily analysis.

The script uses **Pyppeteer** (a headless browser automation tool) to scroll, click, and load hidden data dynamically, and **BeautifulSoup** to parse match details from the HTML page.  
The final data is processed with **Pandas**, merged, deduplicated, and saved automatically.

---

## 🚀 Features
- Scrapes data from Forebet’s **1X2**, **Over/Under 2.5**, and **Both Teams to Score** pages.  
- Automatically scrolls the page and clicks **“MORE”** buttons to load all available matches.  
- Extracts match **date, time, home/away teams, and prediction percentages**.  
- Merges all categories into a single Pandas DataFrame.  
- Removes duplicate entries and saves as a **daily CSV file**.  
- Built using **Pyppeteer**, **BeautifulSoup**, and **Pandas**.

---

## 🧰 Requirements
Make sure you have the following Python libraries installed:

```bash
pip install pyppeteer beautifulsoup4 pandas


⚙️ Setup

Clone this repository:

git clone https://github.com/<your-username>/forebet-data-scraper.git
cd forebet-data-scraper


Open the script and make sure the Chrome executable path is correct:

executablePath=r'C:\Program Files (x86)\Google\Chrome\Application\chrome.exe'


Ensure that your helper module func.py is in the same directory.
(It should contain functions like save_daily_csv(), drop_duplicate(), and others used in the script.)

▶️ Usage
Run the script using:
python your_script_name.py

The program will:

Launch Chrome and open Forebet prediction pages.

Scroll and click “MORE” to load all matches.

Extract prediction data (1X2, Over/Under, BTS/OTS).

Merge all data and remove duplicates.

Save the output as:

/path/to/folder/forebet.csv

📂 Output Example

The saved CSV will look like this:

DATE	TIME	HOME TEAM	AWAY TEAM	HOME PER	DRAW PER	AWAY PER	UNDER 2.5	OVER 2.5	BTS	OTS	NAME
19/10/2025	15:00	Chelsea	Arsenal	45%	30%	25%	55%	45%	60%	40%	Forebet



🧠 Example Use Case

You can use the generated CSV file for:

Building betting strategy models (e.g., with Kelly Criterion or machine learning).

Tracking daily prediction trends from Forebet.

Combining with data from other sources for analysis or automation.



🧩 Tech Stack

Python 3.10+

Pyppeteer – Browser automation

BeautifulSoup4 – HTML parsing

Pandas – Data cleaning and saving

Asyncio / Time – Async execution and timing


🧑‍💻 Author

Ezee Kits

YouTube: Ezee Kits

Focus: Python Programming, Automation, and Data Analysis


📜 License

This project is licensed under the MIT License — feel free to use, modify, and distribute with credit.
