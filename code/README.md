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

 # Conclusion
There are concerns that AirBnB listings are reducing the supply of long-term leases in RPZs, which was shown to be true. The regulation that is being put forward by the government to dramatically decrease the number of AirBnB listings of Entire Units is very useful, however, this should also apply to  private rooms in RPZs, which can be used by college students and young professionals.  Entire Units can be used by families or couples for long-term rent. Furthermore, it is unclear why the landlords choose to put their property on AirBnB when it has been showen that it is more profitable to rent the property when comparing potential AirBnB earning for the year (available nights * daily price) and potential annual rent earnings (rent per month * 12). 

As previously stated, a lot of listings were placed as long-term listings when the pandemic hit, hopefully reducing the pressure on the housing crisis. However, as we continue to come out of the pandemic, we should worry about the return of lack of accommodation in RPZs because of tourist season and increase in AirBnB listings. 

### Limitations
**Data** 
Although there were `r ncol(df)` columns of data in the final data, there are a few vital piece of information are missing. There are Entire Units (houses or apartments) that available for over 90 days of the year in Rent Pressurised Areas, which would require a planning permission. However, this poses a different question: 
- Why don't AirBnB hosts have their properties available all year around? 
- Why do AirBnB hosts choose to place their property on AirBnB and not do long-term leasing?
- Should the government create incentives for AirBnB hosts to lease their property for long-term? 
- Based on above question, perhaps, the government should review obstacles of long-term leasing. 

**Licence / Planning Permission**
After reading Data Dictionary provided AirBnB, it is unclear what is meant by column ‘licence’ in the AirBnB data.  Data analysis at the beginning showed that there are no values in column ‘licence’ and it was dropped from analysis. However, this raises concerns that it be referring to the planning permission required by the local authorities from hosts in RPZ. Lack of planning permissions from the local authorities should be examined. AirBnB should seek planning permissions from their hosts if they meet the criteria for planning permission.  


## Data Sources

Lyons, R. (2021) *Irish Rental Report Q1 2024.* Available at: https://ww1.daft.ie/report/ronan-lyons-2021q2-daftrentalprice?d_rd=1 (Accessed: 28th June 2024).

Residential Tenancies Board (2021) *What are Rent Pressure Zones (RPZ)?* Available at: https://www.rtb.ie/registration-and-compliance/setting-and-reviewing-rent/guide-to-rent-pressure-zones (Accessed: 31 July 2024).


 

# References
Burke, C. (2021) *Rents continue to rise across Ireland as number of rental homes available hits ‘all-time low’, TheJournal.ie.* Available at: https://www.thejournal.ie/daft-rental-report-all-time-low-5596453-Nov2021/ (Accessed: 17 December 2021).

Burke-Kennedy, E. (2021) *Airbnb exodus increases stock of rental property in Dublin by 90%, The Irish Times.* Available at: https://www.irishtimes.com/business/economy/airbnb-exodus-increases-stock-of-rental-property-in-dublin-by-90-1.4654155 (Accessed: 17 December 2021).

Citizensinformation.ie (no date) *Renting your property for short-term lets.* Citizensinformation.ie. Available at: https://www.citizensinformation.ie/en/housing/owning_a_home/home_owners/renting_your_property_for_shortterm_lets.html (Accessed: 17 December 2021).

Pope, C. (2021) *New restrictions likely to reduce supply of short-term rental property, The Irish Times.* Available at: https://www.irishtimes.com/business/new-restrictions-likely-to-reduce-supply-of-short-term-rental-property-1.4653404 (Accessed: 17 December 2021).


