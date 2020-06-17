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

_Last update: 6/16/2020 @ 6:00am_



| date       |   cities |   Elephrame |   CCC |   Count Love |   New York Times |   Wikipedia |
|:-----------|---------:|------------:|------:|-------------:|-----------------:|------------:|
| 2020-05-26 |       11 |           1 |     6 |            7 |                6 |           0 |
| 2020-05-27 |       20 |           0 |    11 |           11 |               11 |           0 |
| 2020-05-28 |       63 |           0 |    41 |           41 |               41 |           9 |
| 2020-05-29 |      182 |           1 |   124 |          128 |               94 |          40 |
| 2020-05-30 |      472 |          35 |   237 |          336 |              337 |         128 |
| 2020-05-31 |      675 |          90 |   225 |          417 |              460 |         154 |
| 2020-06-01 |      551 |          45 |   166 |          298 |              330 |          93 |
| 2020-06-02 |      508 |          39 |   188 |          202 |              296 |          57 |
| 2020-06-03 |      394 |          70 |   138 |           90 |              233 |          49 |
| 2020-06-04 |      341 |          39 |    85 |           98 |              193 |          44 |
| 2020-06-05 |      379 |          85 |   172 |           92 |              172 |          32 |
| 2020-06-06 |      564 |          52 |   309 |          146 |              264 |          44 |
| 2020-06-07 |      341 |          63 |   153 |           94 |              149 |          17 |
| 2020-06-08 |      106 |          15 |    32 |           50 |               34 |           7 |
| 2020-06-09 |       69 |          14 |    30 |           35 |                0 |           6 |
| 2020-06-10 |       56 |          36 |    15 |           18 |                0 |           2 |
| 2020-06-11 |       47 |          12 |     6 |           29 |                0 |           3 |
| 2020-06-12 |       95 |           5 |    41 |           57 |                0 |           7 |
| 2020-06-13 |      104 |          11 |    28 |           77 |                0 |           1 |
| 2020-06-14 |       44 |           4 |    24 |           20 |                0 |           0 |
| 2020-06-15 |        2 |           2 |     0 |            1 |                0 |           0 |


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
