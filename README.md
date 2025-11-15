# Web_Scraping
This project scrapes and processes the 2025 list of the largest technology companies by revenue from the Wikipedia page “List of largest technology companies by revenue”.
Specifically, it focuses on the table for the year 2025.

📝 Project Overview

  Objective: Extract the 2025 ranking of technology companies by revenue, as shown on Wikipedia, and convert it into a clean dataset for analysis.
  
  Source: The table under the “2025 list” section on the Wikipedia page.
  
  Data captured: Company name, revenue in USD (billions), profit in USD (billions), number of employees, country of origin, headquarters location, and the year (2025).

  Use case: Enables analysis of top tech companies’ revenue and employee size for the year 2025, comparison across companies, and potential input into further visualizations or datasets.

🛠️ Technologies & Libraries

   1. Python 3
    
   2. requests — for HTTP fetching of the webpage
    
   3. BeautifulSoup4 — for HTML parsing
    
   4. pandas — for reading HTML tables, cleaning and structuring the data
    
   5. re (regex) — optional, for cleaning numeric fields

📂 Project Structure
project-folder/
│── scrape_2025.py            # Script to scrape the 2025 table
│── requirements.txt          # Dependencies (requests, beautifulsoup4, pandas)
│── tech_companies_2025.csv   # Output dataset for 2025
└── README.md                 # This file

▶️ How to Run
  
  Install dependencies:
  
  pip install -r requirements.txt
    
  Run the scraping script:
  
  python scrape_2025.py
  
  After running the script, the output dataset tech_companies_2025.csv will be available in the project folder.

🧼 Data Cleaning & Processing

  The script locates the “2025 list” table on the source page. 
  
  Extracts the table into a pandas DataFrame.
  
  Adds a Year column with the value 2025.
  
  Cleans the numeric fields: removes characters like “$”, “B” (for billions), commas; converts to float.
  
  Standardizes column names for consistency.

📊 Output Dataset Fields

  The final tech_companies_2025.csv will contain columns such as:
  
  Column Name         	Description
  Company	              Name of the company
  Revenue (USD B)     	Revenue in billions of USD
  Profit (USD B)	      Profit in billions of USD
  Employees	            Number of employees
  Country	              Country of origin
  Headquarters	        Headquarters location
  Year	                2025
  
⚠️ Limitations & Notes

  The dataset covers only the year 2025 (as per table on Wikipedia).
  
  Changes to the Wikipedia page (structure, table format) may require updates to the script.
  
  Some entries may have missing or approximate data due to how Wikipedia presents information and updates.
  
  Revenue is reported in billions of USD as given on the page; no currency conversion is performed.

🔮 Future Improvements
  
  Extend the scraper to include previous years (e.g., 2018-2024) and produce a multi-year dataset.
  
  Add hyperlink extraction (company Wikipedia links) for richer metadata.
  
  Build a Jupyter Notebook to perform exploratory data analysis (EDA) and visualization of the 2025 dataset.

