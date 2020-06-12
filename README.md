# Black Lives Matter events
## Protests following the deaths of George Floyd, Ahmaud Arbery and Breonna Taylor.


This dataset is a hybrid of four excellent sources on BLM protest events:   
* [Elephrame](https://elephrame.com/textbook/BLM/chart)   
* [Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0)  
* [Count Love](https://countlove.org)
* [Wikipedia](https://en.wikipedia.org/wiki/List_of_George_Floyd_protests_in_the_United_States)

Each has been doing the hard work of collecting Black Lives Matter protests based on newspaper and social media accounts. Given the scope of the mobilization and the complicated nature of event data collection, it is not surprising that, while there is a great deal of overlap between the datasets, each has hundreds of unique events.

This combined dataset is constructed using the following process:   
* Download each of the datasets.  For the Wikipedia data, this involves scraping text data from more than thirty pages and converting the written descriptions to tabular data. This aspect is very much a work in progress.   
* Normalize some place names and remove non-US events.  
* Within each dataset, aggregate the number of events within a city on a particular day.   
* Aggregate across datasets for each city-day, retaining the maximum number of events and crowd size reported with one dataset. For example, if the CCC dataset reports two events in Durham on June 1, and the Count Love dataset reports one event on that date, the combined dataset reports two events, under the assumption that the pair of CCC events already include the  Count Love event.   
* The combined dataset includes the following fields:   
   * date - date    
   * city_st - City and State    
   * events - Number of events   
   * size - Number of protesters. Many missing values   
   * size_imp - Number of protesters but missing values have been replaced by 11, a small number of people   
   * CCC - Flag for data from Crowd Counting Consortium   
   * Elephrame - Flag for data from Elephrame   
   * Count Love    - Flag for data from Count Love    
   * urls - list of source urls provided with the original event reports   

Note: This data should not be viewed as final, as cleaning continues. Additionally, the underlying data is still being updated, particularly for very recent events. Use with caution and consult the reference urls.

Thanks to Alisa Robinson,  Tommy Leung and Nathan Perkins, Jeremy Pressman, and Erica Chenoweth for their data collection efforts.

_Last update: 6/11/2020 @ 11:30am_

| date       |   cities |   Elephrame |   CCC |   Count Love |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|------------:|
| 2020-05-26 |        9 |           3 |     4 |            7 |           0 |
| 2020-05-27 |       14 |           6 |     9 |           11 |           0 |
| 2020-05-28 |       49 |          10 |    34 |           40 |          13 |
| 2020-05-29 |      158 |          33 |    99 |          121 |          45 |
| 2020-05-30 |      385 |          69 |   171 |          304 |         174 |
| 2020-05-31 |      453 |          86 |   171 |          306 |         164 |
| 2020-06-01 |      307 |          36 |   134 |          141 |         103 |
| 2020-06-02 |      275 |          35 |   147 |           93 |          64 |
| 2020-06-03 |      240 |          64 |   106 |           69 |          59 |
| 2020-06-04 |      175 |          30 |    39 |           80 |          49 |
| 2020-06-05 |      188 |          77 |    56 |           64 |          32 |
| 2020-06-06 |      230 |          32 |    91 |          105 |          48 |
| 2020-06-07 |      158 |          50 |    60 |           58 |          17 |
| 2020-06-08 |       56 |          12 |     9 |           35 |           4 |
| 2020-06-09 |       37 |          14 |     4 |           21 |           4 |
| 2020-06-10 |       12 |           6 |     4 |            3 |           0 |
## To Do:
* Update daily (current as of 6/11)
* Impute missing attendance
* Add second date for some Wikipedia entries.
* Add city pages to Wikipedia.


## Data Sources:
Leung, Tommy and Nathan Perkins. "Count Love Protest Data." *Count Love*. https://countlove.org

Pressman, Jeremy and Erica Chenoweth. "Crowd Counting Consortium Collection." *Crowd Counting Consortium*. https://sites.google.com/view/crowdcountingconsortium/view-download-the-data

Robinson, Alisa. “Black Lives Matter protests and other demonstrations.” *Elephrame*, https://elephrame.com/textbook/BLM/chart.
