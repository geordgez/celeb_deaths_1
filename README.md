# Celebrity Deaths

Basic cleaning and reformatting of celebrity death data from various sources including [DH Montgomery](http://dhmontgomery.com/2016/12/wikipediadeaths/) and [Kaggle](https://www.kaggle.com/hugodarwood/celebrity-deaths).

The pipeline has been consolidated into [a single notebook](https://github.com/geordgez/celeb_deaths_1/blob/master/src/pt1_batch_scrape.ipynb).

Steps:

1. For summary pages of celebrity deaths by month (and year), batch query Wikipedia API in groups of $n < 50$: the Wikipedia API allows up to 50 queries at a time and API etiquette implicitly limits rate to maximum 1 query/second. This query will have hundreds of entries --> tens of batched queries.

2. Combine the results of all queries and regex and pattern matching to parse out fields, columns, and variables of interest.

3. Collect all resulting entry names (each observation should be a person/figure) and batch query again for wiki page size, date of birth, date of death, etc. This query will have tens of thousands of entries --> thousands of batched queries.
