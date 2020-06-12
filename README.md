# Black Lives Matter events
## Protests following the deaths of George Floyd, Ahmaud Arbery and Breonna Taylor.


This dataset is a hybrid of four excellent sources on BLM protest events:   
* [Elephrame](https://elephrame.com/textbook/BLM/chart)   
* [Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0)  
* [Count Love](https://countlove.org)
* [Wikipedia](https://en.wikipedia.org/wiki/List_of_George_Floyd_protests_in_the_United_States)

Each has been doing the hard work of collecting Black Lives Matter protests based on newspaper and social media accounts. Given the scope of the mobilization and the complicated nature of event data collection (see Fisher et al. 2019), it is not surprising that, while there is a great deal of overlap between the datasets, each has hundreds of unique events.

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

Thanks to Alisa Robinson,  Tommy Leung and Nathan Perkins, Jeremy Pressman, Erica Chenoweth and the CCC & Wikiepdia contributors for their data collection efforts.

_Last update: 6/12/2020 @ 10:30am_



| date       |   cities |   Elephrame |   CCC |   Count Love |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|------------:|
| 2020-05-26 |       10 |           3 |     4 |            7 |           1 |
| 2020-05-27 |       14 |           6 |     9 |           11 |           0 |
| 2020-05-28 |       49 |          10 |    35 |           41 |          12 |
| 2020-05-29 |      157 |          33 |   100 |          121 |          41 |
| 2020-05-30 |      377 |          69 |   176 |          308 |         160 |
| 2020-05-31 |      461 |          86 |   176 |          312 |         166 |
| 2020-06-01 |      307 |          36 |   133 |          147 |          99 |
| 2020-06-02 |      275 |          35 |   149 |           96 |          63 |
| 2020-06-03 |      240 |          64 |   110 |           72 |          53 |
| 2020-06-04 |      181 |          31 |    44 |           87 |          46 |
| 2020-06-05 |      207 |          79 |    65 |           79 |          31 |
| 2020-06-06 |      252 |          35 |   114 |          119 |          45 |
| 2020-06-07 |      169 |          52 |    69 |           66 |          14 |
| 2020-06-08 |       62 |          12 |     9 |           42 |           5 |
| 2020-06-09 |       44 |          15 |     4 |           25 |           6 |
| 2020-06-10 |       26 |          16 |     4 |            7 |           1 |
| 2020-06-11 |       11 |           9 |     0 |            0 |           2 |


## To Do:
* Update daily
* Impute missing attendance
* Add second date for some Wikipedia entries.
* Add city pages to Wikipedia.


## References

Fisher, Dana R., Kenneth T.Andrews, Neal Caren, Erica Chenoweth, Michael T. Heaney, Tommy Leung, Nathan Perkins, and Jeremy Pressman.   2019. ““The Science of Contemporary Street Protest: New Efforts in the United States.” *Science Advances.* https://advances.sciencemag.org/content/5/10/eaaw5461


Leung, Tommy and Nathan Perkins. "Count Love Protest Data." *Count Love*. https://countlove.org

Pressman, Jeremy and Erica Chenoweth. "Crowd Counting Consortium Collection." *Crowd Counting Consortium*. https://sites.google.com/view/crowdcountingconsortium/view-download-the-data

Robinson, Alisa. “Black Lives Matter protests and other demonstrations.” *Elephrame*, https://elephrame.com/textbook/BLM/chart.
