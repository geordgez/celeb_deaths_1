# Celebrity Deaths

Basic cleaning and reformatting of celebrity death data from various sources including [DH Montgomery](http://dhmontgomery.com/2016/12/wikipediadeaths/) and [Kaggle](https://www.kaggle.com/hugodarwood/celebrity-deaths).

Notebook pipeline:

1. [pt1_scrape_summary_pages.ipynb](https://github.com/geordgez/celeb_deaths_1/blob/master/src/pt1_scrape_summary_pages.ipynb) - Scrape the Wikipedia death summary pages for each month and year starting from 2004 and store JSON locally.

2. [pt2_extract_raw_to_csv.ipynb](https://github.com/geordgez/celeb_deaths_1/blob/master/src/pt2_extract_raw_to_csv.ipynb) - Process all the local JSON files and store results into an aggregated CSV file with year, month, name, age, and description info along with fields derived from description info (i.e., cause of death, Nationality).

3. [pt3_scrape_additional_fields.ipynb](https://github.com/geordgez/celeb_deaths_1/blob/master/src/pt3_scrape_additional_fields.ipynb) - Scrape for additional info for each entry (i.e. date of birth, date of death, page size)
