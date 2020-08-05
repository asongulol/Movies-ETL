# Extract Transfom Load (ETL) of Movie Data

ETL is an essential function preparatory to data analysis. Data from different sources are extracted, cleaned and loaded into a database for later analysis. Understandably, this can be a tedious and inexact process that relies on assumptions that allow us to get to an acceptable degree of certainty as to the data's integrity and usefulness while balancing time necessary for analysis and coding. Therefore, certain assumptions are necessary to give us a cut-off point of the cleaning that we would do to prevent the process from taking too much time and coding. 

## Assumptions

It is important to list your assumptions and reasons for these assumptions so that later on you can review them later if the data is erroneous or incorrect.

The following assumptions were used in the ETL process from the Wikipedia, Kaggle and Movielens data:

1. __Always assume that the data you are using has no backup.__ This assumption will prevent you from making destructive edits of the data files that you are using which in turn allows you to go back several steps when the assumptions that you are making prove to be incorrect as they sometimes do.

2. __The 7,311 movies in the database is a reasonable number for the dataset.__ A check of the number of movie records in the raw file indicates 7,311 records, which means over 30 years this equates to about 240 movies per year or about 5 movies per week. If we assume that there are 2 major movies for every 3 indie movies then the number of movies in the database is reasonable.

3. __The 5,485 movies with box office data is reasonable.__ It’s about 5,500 movies out of 7,000, which is a little more than three-quarters. Box office data is reported by multiple sources, and we’d expect some percentage of them to not have reliable box office numbers, or for smaller indie films to not have any box office numbers published at all. Twenty-five percent would mean the bottom quartile of movies has no box office data, which seems a little high, but for every movie missing box office data, there are a little more than three movies that do have box office data. Also, 5,500 is still a good number of movies to perform analysis on (more than 180 movies per year).

4. __It is not necessary to parse the remaining 30 budget values.__ As the module states, "The juice isn't worth the squeeze." here are some reasons why we did not continue to parse the remaining values:
  - Some of them don’t even have numeric values, and those that do tend to be in a different currency. Converting currencies can be difficult, for example, what conversion rates do you use and for what dates, etc.
  - Some values could be parsed into useful data without currency conversion, but they are so few at most 1% of the data that it's not worth it.
  
5. __Kaggle data is more consistent and useable than Wikipedia data.__ Based on the analysis it appears that Kaggle data has more consistent and more readily usable data and therefore in cases where the data is the same, Wikipedia has been dropped or used only to fill zeros in the Kaggle data. This assumption is based on scatter plot data which show a lot more outliers in the Wikipedia data as compared to the Kaggle data. 

6. __Columns with less than 90% null values are not useful.__ Aout half the columns have more than 6,000 null values. We made a list of columns that have less than 90% null values and use those to trim down our dataset. We are assuming that this artificial cut-off will not remove data that might be useful for analysis in the future.
 

