# Extract Transfom Load (ETL) of Movie Data

ETL is an essential function preparatory to data analysis. Data different sources are extracted, cleaned and loaded into a database for later analysis. Understandably, this can be a tedious and inexact process that relies on assumptions that allow us to get to an acceptable degree of certainty as to the data's integrity and usefulness. Therefore, certain assumptions are necessary to give us a cut-off point of the cleaning that we would do to prevent the process from taking too much time and coding. 

## Assumptions

It is important to list your assumptions and reasons for these assumptions so that later on you can review them later if the data is erroneous or incorrect.

The following assumptions were used in the ETL process from the Wikipedia, Kaggle and Movielens data:

1. __Number of movies in the database are reasonable.__ A check of the number of movie records in the raw file indicates 7,311 records, which means over 30 years this equates to about 240 movies per year or about 5 movies per week. If we assume that there are 2 major movies for every 3 indie movies then the number of movies in the database is reasonable.

