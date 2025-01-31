## Project structure
- data - Source data
    - **douban-data.txt** - Douban movie list (Chinese)
    - **filmweb_1939_2023.csv** - Filmweb movie list (Polish)
    - **imdb-data.csv** - Imdb movie list (English)
- results - Processed data
    - **ratings.csv** - Combined, cleaned and transformed data from 3 movie sources
    - **plots.json** - Scrapped imdb plot description for movies included in **ratings**
    - **cluster_terms.csv** - Clusters produced from TF-IDF Transformation of **plots**
    - **id_to_cluster.csv** - Association of **plots** with their **cluster_terms**
- **ratings.ipynb** - Cleaning, transforming and combining ratings of 3 movie databases
- **scraper.ipynb** - Web scraper using scrapy library to fetch the latest plot description of movies from IMDB.com
- **plot-analyzer.ipynb** - Cleans the plots data, uses TF-IDF transformation on texts, groups clusters using k-means algorithm
- **dashboard.ipynb** - A place to visualize the results of ratings

## Requirements
- python3 (tested on 3.13.1)
- Jupiter notebook/Visual Studio Code (anything that opens .ipynb files)
- pandas
- scrapy
- nltk
- scikit-learn

## How to run
Install python3 and requirements using pip install, then execute all .ipynb files in this order:    
**ratings** -> **scraper** -> **plot-analyzer** -> **dashboard**

## Sources
filmweb: https://www.kaggle.com/code/kfc667/quick-filmweb-eda   
imdb: https://www.kaggle.com/datasets/octopusteam/full-imdb-dataset   
douban: https://www.kaggle.com/datasets/fengzhujoey/douban-datasetratingreviewside-information     
scraping source: https://imdb.com/