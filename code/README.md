## Files submitted
- listings.csv - AirBnB listings in Ireland from the beginning of AirBnB operating in Ireland

- calendar.csv - AirBnB listings from 23rd October 2021 to 21st October 2021 (dates not chosen by student, supplied by AirBnB), contains 9 million rows.

- rent_pressure_zones.csv -RTZs (RPZs) were developed by the Irish government to tackle rising rents lack of affordable rental units. These are areas located in parts of the country where rents are the highest and rising, and where households have the greatest difficulty finding affordable accommodation (Residential Tenancies Board, 2021). The csv was manually created from RTB website. 

- rent_in_ireland.csv - The website daft.ie is the leading property website in Ireland, which publishes reports on the Irish housing market every quarter. For this next dataset, the report Q2 2021 was used to find out the rent in each city and county in Ireland (Lyons, 2021). The csv was manually created from the report. 

## Stage 1
Due to the 9 million rows in calendar.csv, it was decided to treat this dataset outside of this analysis due to the size of it. 

- calendar_df.Rmd - Code to treat calendar.csv and create the two datasets below to analyse in this report
- summarise_df.csv - A new dataset from calendar.csv  was created, where listings were examined by availability for each month within a year (23rd October 2021 to 21st October 2022).
- available_nights_df.csv - A new dataset summarising the number of available nights for each listing in a year (23rd October 2021 to 21st October 2022).
- calendar_df.html - Document presents calendar_df.Rmd in HTML

## Stage 2
** DOCUMENT cleaning processes. **

## Stage 3
Based on previous work (in archive), I am aware of the distributions and frequencies of the data. Stage 3 was for storytelling report. 


# Introduction
The aim of this project is tell a story about AirBnB listings through graphs in plotly package and dplyr packages in R.

Housing Crisis in Ireland is a hot topic at the moment, which is affecting vast number of people, both young and old. AirBnB is the leading short-term lease of a private property website, where individuals place their homes on AirBnB to lease it to tourists on a short-term basis. 

In this report, I will be examining the impact of AirBnB on Irish Rental Crisis, by analysing AirBnB listings data by examining the RTZs from Residential Tenancies Board, Irish housing report from Daft.ie and the Homelessness Report from the Irish government. 

To fully take advantage the beauty of plotly interactivity, please knit this file into a HTML file. This will allow you, as the reader, to interact with the graphs. If the project in knitted into a word document, then the graphs will not be displayed, only tables will be displayed, which were created using dplyr.  


# Business Understanding
### Housing Crisis
There is a huge housing crisis in Ireland, which has been defined as a shortage of affordable accommodation for renting or buying.  Irish government has made attempts to reduce the housing crisis with plans of affordable and social housing, however, lobbyists criticise the government for late intervention and lack of innovative solutions. Both young adults (under 35 years old) and more older adults are worrying about not being able to afford a home because of rent prices and increasing house prices. 

### Rent Report
Rent prices all over Ireland are increasing and Irish people worry about the affordability of rent, considering in areas like Dublin, individuals can pay up to 50% of their salary for rent. This is very nerve-wracking experience for the tenants.
Daft.ie is the leading property website in Ireland, which publishes reports on the Irish housing market every quarter. For this next dataset, the report Q2 2021 was used to find out the rent in each town and city in Ireland (Lyons, 2021) . 

### Rent Pressure Zones
To deal with rising rents and lack of affordable rental units, the government introduced Rent Pressure Zones (RPZs). These are areas located in parts of the country where rents are highest and rising, and where households have the greatest difficulty finding affordable accommodation (Residential Tenancies Board, 2021).  Currently, there are six Local Authority Areas and 48 Local Electoral Areas (LEA) which have been designated as RTZs.  In these areas, the rent cannot be increased by more than general inflation. The list is available to be viewed on Residential Tenancies Board (RTB) (Residential Tenancies Board, 2021). 


### AirBnB
AirBnB hosts and AirBnB, itself, have been strongly criticised for the increase of listings for short-term leasing for tourism. It has been reported that over 30,000 Irish listings on the site in Ireland for short-term lease (Pope, 2021). The article from The Irish Times continues to state that nearly half of those listings are rooms in private homes and over 10,000 entire homes are available all-year-round.

There have been talks of the Irish government to "bring legislation to create new measures that would target at least some of those properties and may see them return to the long-term rental market.  Any moves which curtail the availability of AirBnB in popular tourism destinations around the country are likely to have a knock-on impact on accommodation availability and prices once international tourism resumes in a significant way in the post-pandemic period" (Pope, 2021). At the start of the pandemic,  figures from estate agent Sherry FitzGerald show the number of properties available for rent in Dublin rose from 1,593 in November 2019 to 3,039 by the end March 2020  (Burke-Kennedy, 2021).

### Potential Long-Term Use of Accommodation Type at AirBnB
- Entire Rental Unit – this could be a house or an apartment.  For this report, entire rental units will be viewed as a possible long-term accommodation for a family.
- Private Room – this is a private room in a shared house.  This type of accommodation is usually used by students for the academic months of the year or young professionals (all year around).

# Data Understanding

Please look at Stage 2 and Stage 3 for Data Understanding.

 
## Data Sources

Lyons, R. (2021) *Irish Rental Report Q2 2021.* Available at: https://ww1.daft.ie/report/ronan-lyons-2021q2-daftrentalprice?d_rd=1 (Accessed: 17 December 2021).

Residential Tenancies Board (2021) *What are Rent Pressure Zones (RPZ)?* Available at: https://www.rtb.ie/during-a-tenancy/rent-review-in-a-rent-pressure-zone-rpz?gclid=Cj0KCQiAzfuNBhCGARIsAD1nu-8YhjJPsVbhgWjuM0et4lZX2ansT4b4XkLEEx9G63vDiVsptSzv8toaAkdDEALw_wcB (Accessed: 19 December 2021).


