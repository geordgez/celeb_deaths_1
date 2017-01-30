# Celebrity Deaths

Basic cleaning and reformatting of celebrity death data from various sources including [DH Montgomery](http://dhmontgomery.com/2016/12/wikipediadeaths/) and [Kaggle](https://www.kaggle.com/hugodarwood/celebrity-deaths).

Notebook pipeline:
1. Scrape the Wikipedia death summary pages for each month and year starting from 2004 and store JSON locally (get_monthly_death_list_1.ipynb).
2. Process all the local JSON files and store results into an aggregated CSV file with year, month, name, age, and description info along with fields derived from description info (i.e., cause of death, Nationality).
3. Scrape for additional info for each entry (i.e. date of birth, date of death, page size)
