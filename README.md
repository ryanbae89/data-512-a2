# Bias in Data

The prototype framework of this README.md file is taken from the instructor's tutorial repo [here](https://github.com/Ironholds/data-512-a2).

## Goal

This project is the second assignment of the DATA 512 Ethics course. This assignment aims to study bias in data by looking at Wikipedia articles of politicians from different countries. More specifically, the project aims to look at how the coverage of politicians and quality of articles of politicians varies across countries. 

The analysis calculates the following metrics for each country from Wikipedia articles of their political figures:

* Proportion of number of Wikipedia articles about their political figures to the population.

* Percentage of number of Wikipedia articles about political figures that are "high-quality" for each country. This is measured using Wikipedia's machine learning service ORES API. 

The goal is to gain a better understanding of biases in data and its consequences through this exercise.

The specific guidline to the assignment from which the goals of this project in this README.md file borrows, can be found [here](https://wiki.communitydata.cc/Human_Centered_Data_Science_(Fall_2018))

## Data Sources

The data comes from two different sources:

* [Politicans by Country](https://figshare.com/articles/Untitled_Item/5513449)

This dataset contains the revision ID and names of each politician wikipedia article and the country name. This dataset was downloaded into csv file `page_data.csv`.

* [Country Population Data](https://www.prb.org/international/indicator/population/table/)

The country population dataset comes from PRB International Data. The dataset contains the country name and population of that country. It was downloaded into csv file `WPDS_2018_data.csv`.

The [ORES API](https://www.mediawiki.org/wiki/ORES) was used to obtain the article quality feature.

## Resources

This analysis was done using Python 3.6 running in a Jupyter Notebook. 

The documentation for Python 3.6 can be found [here](https://docs.python.org/3.6/), and the documentation for Jupyter Notebook can be found [here](https://jupyter-notebook.readthedocs.io/en/latest/).

Object Revision Evaluation Service (ORES) was used to obtain the article quality feature. The documentation for using this API can be found [here](https://ores.wikimedia.org/).

The API call function in the iPython notebook used a code block from the tutorial written by the course instructor Jonathan Morgan:

https://github.com/Ironholds/data-512-a2/blob/master/hcds-a2-bias_demo.ipynb

## Final Data File

Running the iPython notebook with `page_data.csv` and `WPDS_2018_data.csv` files creates the final table containing the following schema:

| country  | article_name  |  revision_id | article_quality | population |
|---------:|:-------------:|-------------:|----------------:|-----------:|
| Chad	   |Bir I of Kanem |  355319463	  | Stub            | 15400000.0 |

This is saved to csv file named `final_data.csv`. 

## License/Terms of Use

The code in this repository is licensed under [MIT License](https://opensource.org/licenses/MIT). 

For licensing information about the politicians by country data source, please refer to [figshare's webpage](https://figshare.com/privacy) for more information and their terms of use policy. 

For licensing information about the country population data source, please refer to [PRB's webpage](https://www.prb.org/) for their site-wide general policy.

The content accessed via Wikimedia's API is licensed under the [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) and [GFDL](https://www.gnu.org/copyleft/fdl.html) licenses, and you irrevocably agree to release modifications or additions made through this API under these licenses.

When reproducing the results, please take a look at the [Wikimedia Terms of Use](https://foundation.wikimedia.org/wiki/Terms_of_Use/en) for more information. 