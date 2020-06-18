# Black Lives Matter events
## Protests following the deaths of George Floyd, Ahmaud Arbery and Breonna Taylor.


This dataset is a hybrid of five excellent sources on BLM protest events:   
* [Elephrame](https://elephrame.com/textbook/BLM/chart)   
* [Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0)  
* [Count Love](https://countlove.org)
* [New York Times](https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html)
* [Wikipedia](https://en.wikipedia.org/wiki/List_of_George_Floyd_protests_in_the_United_States)

Each has been doing the hard work of collecting Black Lives Matter protests based on newspaper and social media accounts. Given the scope of the mobilization and the complicated nature of event data collection (see Fisher et al. 2019), it is not surprising that, while there is a great deal of overlap between the datasets, each has hundreds of unique events.

This combined dataset is constructed using the following process:   
* Download each of the datasets.  For the Wikipedia data, this involves scraping text data from more than thirty pages and converting the written descriptions to tabular data. This aspect is very much a work in progress.  The New York Times listing draws on their own research, plus the [Count Love](https://countlove.org) and [Alex Smith](https://www.creosotemaps.com/blm2020/) event listings.
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
   * wikipedia    - Flag for data from Wikipedia   
   * New York Times   - Flag for data from New York Times   
   * urls - list of source urls provided with the original event reports   

Note: This data should not be viewed as final, as cleaning continues. Additionally, the underlying data is still being updated, particularly for very recent events. Use with caution and consult the reference urls.

_Last update: 6/18/2020 @ 10:00am_



| date       |   cities |   Elephrame |   CCC |   Count Love |   New York Times |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|-----------------:|------------:|
| 2020-05-26 |       10 |           1 |     0 |            7 |                6 |           0 |
| 2020-05-27 |       17 |           0 |     0 |           11 |               11 |           0 |
| 2020-05-28 |       58 |           0 |     0 |           41 |               41 |           8 |
| 2020-05-29 |      164 |           0 |     0 |          128 |               94 |          39 |
| 2020-05-30 |      450 |           0 |     0 |          340 |              337 |         128 |
| 2020-05-31 |      647 |          75 |     0 |          428 |              460 |         156 |
| 2020-06-01 |      556 |          48 |   168 |          310 |              330 |          93 |
| 2020-06-02 |      539 |          38 |   193 |          276 |              297 |          58 |
| 2020-06-03 |      422 |          70 |   138 |          150 |              233 |          51 |
| 2020-06-04 |      355 |          39 |   101 |          101 |              193 |          45 |
| 2020-06-05 |      385 |          85 |   176 |           95 |              172 |          36 |
| 2020-06-06 |      569 |          47 |   316 |          152 |              264 |          47 |
| 2020-06-07 |      346 |          62 |   164 |           96 |              149 |          19 |
| 2020-06-08 |      107 |          15 |    34 |           51 |               34 |           7 |
| 2020-06-09 |       71 |          15 |    30 |           36 |                0 |           6 |
| 2020-06-10 |       59 |          36 |    17 |           21 |                0 |           2 |
| 2020-06-11 |       49 |          12 |     7 |           32 |                0 |           4 |
| 2020-06-12 |      105 |           9 |    48 |           61 |                0 |           9 |
| 2020-06-13 |      122 |          16 |    37 |           89 |                0 |           1 |
| 2020-06-14 |       83 |          30 |    28 |           38 |                0 |           1 |
| 2020-06-15 |       16 |           2 |     2 |           14 |                0 |           0 |
| 2020-06-16 |       16 |           2 |     2 |           12 |                0 |           0 |
| 2020-06-17 |        4 |           2 |     2 |            0 |                0 |           0 |


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

Burch, Audra D. S., Weiyi Cai, Gabriel Gianordoli, Morrigan McCarthy and Jugal K. Patel. "How Black Lives Matter Reached Every Corner of America" _The New York Times_ June 6, 2013. https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html
