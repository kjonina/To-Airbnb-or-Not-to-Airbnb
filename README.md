# Better Than Renting? To Airbnb or Not to Airbn.... 

In July 2024, in the process of revision. 

### Research Question
1. How many entire units and private rooms Airbnb are in RPZs?
2. Based on the availability \* price, what is the potential annual income from the Airbnb?
3. When compared to the potential annual income from rent, how many landlords would earn more by long-term leasing the listing?
4. How much MORE money could each of those landlords be earning if they long-term leased the property?


# Introduction
The aim of this report is tell a story about AirBnB listings through graphs in plotly package and dplyr packages in R.

Rental Crisis in Ireland is a hot topic at the moment, which is affecting vast number of people, both young and old. AirBnB is the leading short-term lease of a private property website, where individuals place their homes on AirBnB to lease it to tourists on a short-term basis. 

In this report, I will be examining the impact of AirBnB on Irish Rental Crisis, by analysing AirBnB listings data by examining the RTZs from Residential Tenancies Board, Irish housing report from Daft.ie and the Homelessness Report from the Irish government. 

To fully take advantage the beauty of plotly interactivity, please knit this file into a HTML file. This will allow you, as the reader, to interact with the graphs. If the report in knitted into a word document, then the graphs will not be displayed, only tables will be displayed, which were created using dplyr.  

# Business Understanding
### Rental Crisis
There is a huge Rental Crisis in Ireland, which has been defined as a shortage of affordable accommodation for renting.  Irish government has made attempts to reduce the Rental Crisis with plans of affordable and social housing, however, lobbyists criticise the government for late intervention and lack of innovative solutions. Both young adults (under 35 years old) and more older adults are worrying about not being able to afford a home because of rent prices and increasing house prices. 

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

## [Analyzing the Influence of Airbnb on Irish Property Prices Report](https://public.tableau.com/app/profile/karina.jonina/viz/To-Rent-or-Not-To-Rent/Dashboard)

<img src='https://github.com/kjonina/icons/To-Airbnb-Tableau.png'/></a>


## Data Sources

Lyons, R. (2024) *Irish Rental Report Q1 2024.* Available at: https://ww1.daft.ie/report/ronan-lyons-2021q2-daftrentalprice?d_rd=1 (Accessed: 28th June 2024).

Residential Tenancies Board (2021) *What are Rent Pressure Zones (RPZ)?* Available at: https://www.rtb.ie/registration-and-compliance/setting-and-reviewing-rent/guide-to-rent-pressure-zones (Accessed: 31 July 2024).


 