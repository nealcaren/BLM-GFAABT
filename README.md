# Black Lives Matter events
## Protests following the deaths of George Floyd, Ahmaud Arbery and Breonna Taylor.


This dataset is a hybrid of three excellent sources on BLM protest events:   
* [Elephrame](https://elephrame.com/textbook/BLM/chart)   
* [Crowd Counting Consortium](https://sites.google.com/view/crowdcountingconsortium/view-download-the-data?authuser=0)  
* [Count Love](https://countlove.org)

Each has been doing the hard work of collecting Black Lives Matter protests based on newspaper and social media accounts. Given the scope of the mobilization and the complicated nature of event data collection, it is not surprising that, while there is a great deal of overlap between the datasets, each has hundreds of unique events.

This combined dataset is constructed using the following process:   
* Download each of the datasets.     
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

| date       |   cities |   Elephrame |   CCC |   Count Love |
|:-----------|---------:|------------:|------:|-------------:|
| 2020-05-26 |        9 |           3 |     4 |            7 |
| 2020-05-27 |       14 |           6 |     8 |           11 |
| 2020-05-28 |       44 |          10 |    33 |           40 |
| 2020-05-29 |      136 |          33 |    92 |          121 |
| 2020-05-30 |      333 |          69 |   146 |          304 |
| 2020-05-31 |      386 |          85 |   168 |          306 |
| 2020-06-01 |      238 |          36 |   130 |          141 |
| 2020-06-02 |      229 |          35 |   144 |           93 |
| 2020-06-03 |      193 |          64 |    97 |           69 |
| 2020-06-04 |      132 |          30 |    35 |           80 |
| 2020-06-05 |      160 |          77 |    49 |           64 |
| 2020-06-06 |      182 |          32 |    76 |          105 |
| 2020-06-07 |      140 |          51 |    53 |           58 |
| 2020-06-08 |       49 |          12 |     5 |           35 |
| 2020-06-09 |       32 |          14 |     3 |           20 |
| 2020-06-10 |       10 |           6 |     2 |            3 |

## To Do:
* Update daily (current as of 6/11)
* Inpute missing attendance
* Better event matching
* Add wikipedia events


## Data Sources:
Leung, Tommy and Nathan Perkins. "Count Love Protest Data." *Count Love*. https://countlove.org

Pressman, Jeremy and Erica Chenoweth. "Crowd Counting Consortium Collection." *Crowd Counting Consortium*. https://sites.google.com/view/crowdcountingconsortium/view-download-the-data

Robinson, Alisa. “Black Lives Matter protests and other demonstrations.” *Elephrame*, https://elephrame.com/textbook/BLM/chart.
