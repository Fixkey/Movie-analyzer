## Project structure
- data - source data
    - **douban-data.txt** - douban movie list
    - **filmweb_1939_2023.csv** - filmweb movie list
    - **imdb-data.csv** - imdb movie list
- results - processed data
    - **ratings.csv** - combined, cleaned and transformed data from 3 movie sources
    - **plots.json** - scrapped imdb plot description for movies included in **ratings**
    - **cluster_terms.csv** - clusters produced from TF-IDF Transformation of **plots**
    - **id_to_cluster.csv** - association of **plots** with their **cluster_terms**
- **ratings.ipynb** - cleaning, transforming and combining ratings of 3 movie databases
- **scraper.ipynb** - Web scraper using scrapy library to fetch the latest plot description of movies from IMDB.com
- **plot-analyzer.ipynb** - Cleans the plots data, uses TF-IDF transformation on texts, groups clusters using k-means algorithm.
- **dashboard.ipynb** - a place to visualize the results

## Requirements
- python3 (tested on 3.13.1)
- pandas
- scrapy
- 

## How to run
Install python3 and requirements using pip install, then execute all .ipynb files in this order:    
**ratings** -> **scraper** -> **plot-analyzer** -> **dashboard**

## Sources
filmweb: https://www.kaggle.com/code/kfc667/quick-filmweb-eda   
imdb: https://www.kaggle.com/datasets/octopusteam/full-imdb-dataset   
douban: https://www.kaggle.com/datasets/fengzhujoey/douban-datasetratingreviewside-information