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

_Last update: 6/13/2020 @ 6:30am_



| date       |   cities |   Elephrame |   CCC |   Count Love |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|------------:|
| 2020-05-26 |        8 |           1 |     4 |            7 |           0 |
| 2020-05-27 |       13 |           0 |    10 |           11 |           0 |
| 2020-05-28 |       50 |           9 |    36 |           41 |          11 |
| 2020-05-29 |      160 |          33 |   104 |          122 |          41 |
| 2020-05-30 |      380 |          70 |   187 |          310 |         154 |
| 2020-05-31 |      490 |          89 |   189 |          351 |         164 |
| 2020-06-01 |      324 |          40 |   136 |          165 |         100 |
| 2020-06-02 |      281 |          37 |   155 |           99 |          61 |
| 2020-06-03 |      240 |          64 |   112 |           74 |          52 |
| 2020-06-04 |      184 |          33 |    46 |           88 |          46 |
| 2020-06-05 |      221 |          80 |    84 |           82 |          34 |
| 2020-06-06 |      277 |          37 |   145 |          123 |          45 |
| 2020-06-07 |      182 |          52 |    78 |           73 |          14 |
| 2020-06-08 |       63 |          12 |    11 |           43 |           5 |
| 2020-06-09 |       47 |          14 |    10 |           27 |           4 |
| 2020-06-10 |       31 |          19 |     6 |            9 |           1 |
| 2020-06-11 |       15 |          10 |     2 |            1 |           3 |
| 2020-06-12 |       32 |           4 |    30 |            0 |           0 |


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
