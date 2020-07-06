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

_Last update: 7/2/2020 @ 10:00am_


| date       |   cities |   Elephrame |   CCC |   Count Love |   New York Times |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|-----------------:|------------:|
| 2020-05-26 |       11 |           1 |     6 |            7 |                6 |           0 |
| 2020-05-27 |       20 |           0 |    11 |           11 |               11 |           0 |
| 2020-05-28 |       63 |           0 |    44 |           42 |               41 |           7 |
| 2020-05-29 |      186 |           0 |   134 |          135 |               94 |          38 |
| 2020-05-30 |      492 |           0 |   346 |          352 |              337 |         139 |
| 2020-05-31 |      689 |           0 |   454 |          451 |              460 |         166 |
| 2020-06-01 |      581 |           0 |   338 |          344 |              331 |         101 |
| 2020-06-02 |      564 |           0 |   252 |          341 |              297 |          65 |
| 2020-06-03 |      469 |           1 |   292 |          274 |              233 |          57 |
| 2020-06-04 |      441 |          19 |   236 |          262 |              192 |          50 |
| 2020-06-05 |      485 |          82 |   291 |          284 |              173 |          43 |
| 2020-06-06 |      699 |          51 |   487 |          410 |              262 |          59 |
| 2020-06-07 |      411 |          64 |   270 |          203 |              149 |          34 |
| 2020-06-08 |      123 |          15 |    57 |           59 |               34 |           8 |
| 2020-06-09 |       85 |          15 |    44 |           41 |                0 |           9 |
| 2020-06-10 |       76 |          35 |    33 |           29 |                0 |           3 |
| 2020-06-11 |       93 |          12 |    56 |           37 |                0 |           7 |
| 2020-06-12 |      160 |          14 |   121 |           67 |                0 |          13 |
| 2020-06-13 |      249 |          25 |   203 |          110 |                0 |           2 |
| 2020-06-14 |      147 |          48 |   101 |           45 |                0 |           2 |
| 2020-06-15 |       30 |           6 |     4 |           23 |                0 |           1 |
| 2020-06-16 |       32 |           6 |     3 |           27 |                0 |           0 |
| 2020-06-17 |       32 |          15 |     5 |           14 |                0 |           0 |
| 2020-06-18 |       24 |           5 |     4 |           16 |                0 |           0 |
| 2020-06-19 |      255 |          26 |   191 |           49 |                0 |           0 |
| 2020-06-20 |       53 |          20 |     7 |           30 |                0 |           2 |
| 2020-06-21 |       36 |          21 |     2 |           19 |                0 |           0 |
| 2020-06-22 |       22 |          13 |     1 |           13 |                0 |           0 |
| 2020-06-23 |       17 |           2 |     3 |           15 |                0 |           0 |
| 2020-06-24 |       13 |           4 |     1 |            9 |                0 |           0 |
| 2020-06-25 |       26 |           1 |     1 |           22 |                0 |           3 |
| 2020-06-26 |       20 |           1 |     3 |           17 |                0 |           0 |
| 2020-06-27 |       71 |          32 |     9 |           43 |                0 |           1 |
| 2020-06-28 |       29 |          10 |     4 |           16 |                0 |           0 |
| 2020-06-29 |       20 |          15 |     0 |            7 |                0 |           1 |
| 2020-06-30 |       18 |           9 |     1 |           12 |                0 |           0 |
| 2020-07-01 |       18 |           9 |     0 |           13 |                0 |           0 |
| 2020-07-02 |       23 |          11 |     0 |           14 |                0 |           0 |
| 2020-07-03 |       21 |           1 |     0 |           20 |                0 |           0 |
| 2020-07-04 |       57 |          17 |     0 |           45 |                0 |           2 |
| 2020-07-05 |       22 |          21 |     0 |            5 |                0 |           0 |


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
