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

_Last update: 6/30/2020 @ 10:00am_


| date       |   cities |   Elephrame |   CCC |   Count Love |   New York Times |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|-----------------:|------------:|
| 2020-05-26 |       11 |           1 |     6 |            7 |                6 |           0 |
| 2020-05-27 |       20 |           0 |    11 |           11 |               11 |           0 |
| 2020-05-28 |       62 |           0 |    42 |           42 |               41 |           7 |
| 2020-05-29 |      186 |           0 |   126 |          135 |               94 |          38 |
| 2020-05-30 |      489 |           0 |   342 |          351 |              337 |         132 |
| 2020-05-31 |      682 |           0 |   444 |          449 |              460 |         164 |
| 2020-06-01 |      573 |           0 |   327 |          340 |              331 |          98 |
| 2020-06-02 |      557 |           8 |   239 |          337 |              296 |          64 |
| 2020-06-03 |      475 |          69 |   246 |          266 |              233 |          57 |
| 2020-06-04 |      572 |          33 |   247 |          251 |              192 |          48 |
| 2020-06-05 |      466 |          81 |   199 |          263 |              173 |          41 |
| 2020-06-06 |      629 |          47 |   479 |          283 |              262 |          55 |
| 2020-06-07 |      362 |          62 |   178 |          103 |              149 |          28 |
| 2020-06-08 |      120 |          18 |    41 |           56 |               34 |           7 |
| 2020-06-09 |       80 |          17 |    40 |           40 |                0 |           6 |
| 2020-06-10 |       75 |          38 |    32 |           27 |                0 |           3 |
| 2020-06-11 |       90 |          13 |    56 |           34 |                0 |           5 |
| 2020-06-12 |      158 |          15 |   121 |           65 |                0 |          12 |
| 2020-06-13 |      246 |          25 |   201 |          106 |                0 |           2 |
| 2020-06-14 |      142 |          49 |    98 |           44 |                0 |           2 |
| 2020-06-15 |       30 |           7 |     4 |           22 |                0 |           0 |
| 2020-06-16 |       30 |           5 |     3 |           25 |                0 |           0 |
| 2020-06-17 |       31 |          15 |     5 |           13 |                0 |           0 |
| 2020-06-18 |       24 |           5 |     4 |           16 |                0 |           0 |
| 2020-06-19 |      252 |          25 |   190 |           47 |                0 |           0 |
| 2020-06-20 |       50 |          19 |     6 |           27 |                0 |           2 |
| 2020-06-21 |       35 |          21 |     2 |           18 |                0 |           0 |
| 2020-06-22 |       21 |          13 |     1 |           12 |                0 |           0 |
| 2020-06-23 |       14 |           1 |     3 |           12 |                0 |           0 |
| 2020-06-24 |       12 |           3 |     1 |            8 |                0 |           0 |
| 2020-06-25 |       22 |           0 |     1 |           20 |                0 |           2 |
| 2020-06-26 |       17 |           1 |     2 |           14 |                0 |           0 |
| 2020-06-27 |       56 |          19 |     8 |           38 |                0 |           1 |
| 2020-06-28 |       12 |           0 |     3 |           10 |                0 |           0 |
| 2020-06-29 |        1 |           0 |     0 |            1 |                0 |           0 |


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
