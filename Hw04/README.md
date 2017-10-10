README
================
Abdullah Farouk
2017-10-10

I highlight the various tasks I carried out, along with my thoughts on what was easy and difficult for me to achieve. Please refer [here](https://github.com/navysealtf9k/STAT545-hw-Farouk-Abdullah/blob/master/Hw03/hwo03.md) if you want to see what my analysis looks like.

Progress Report
===============

This format was thought of after peer reviewing the following [assignment](https://github.com/Jenncscampbell/STAT545-hw-Campbell-Jennifer/tree/master/hw02)

Make a tibble with one row per year and columns for life expectancy for two or more countries. Use knitr::kable() to make this table look pretty in your rendered homework.Take advantage of this new data shape to scatterplot life expectancy for one country against that of another.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-   This took me a long time to complete as I did not understand how to use the gather and spread functions.
-   Didnt clearly understand what "columns for two countries" meant exaclty. Took it as produce a table with two columns for two different countries with each cell corresponding to the life expectancy of the different countries for a particular year.
-   The table I created allowed me to create a very interesting plot. I played around with various arguements within the theme function to try and make it look better.
-   Used knittr to try and make my table pretty.
-   Converted population into a fraction of a billion to make my numbers easier to understand on the grpah legend.
-   I made use of a neat method shown in class to convert my legends into a form that is easier to read.
-   I tried changing the default colour schemes but was unsuccessful in doing so.

Create a second data frame, complementary to Gapminder. Join this with (part of) Gapminder using a dplyr join function and make some observations about the process and result. Explore the different types of joins. Examples of a second data frame you could build: One row per country, a country variable and one or more variables with extra info, such as language spoken, NATO membership, national animal, or capitol city. If you really want to be helpful, you could attempt to make a pull request to resolve this issue, where I would like to bring ISO country codes into the gapminder package. One row per continent, a continent variable and one or more variables with extra info, such as northern versus southern hemisphere.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

-   This task was relatively easier to manage and carry out.
-   Chose to bring in the ISO code with every country in the gapminder dataset.
-   Created a dataset for this purpose by using information from a dataset in r called countrycodes data.
-   Made use of filtering joins to perform checks on my datasets.
-   Experimented with inner and full join to see which would give me the ISO codes for *ALL* the countries in my dataset

Explore the base function merge(), which also does joins. Compare and contrast with dplyr joins.
------------------------------------------------------------------------------------------------

-   Used the merge function to compare it's output with that of my join function calls earlier. Did not have any trouble calling on this function.
-   Tried using the match function. It's output differed from those of the merge and join function calls. Whilst it was interesting, I found it difficult to interpret some of the results I got.

NOTE
----

All citations for my code are in my link [here](https://github.com/navysealtf9k/STAT545-hw-Farouk-Abdullah/blob/master/Hw03/hwo03.md)
