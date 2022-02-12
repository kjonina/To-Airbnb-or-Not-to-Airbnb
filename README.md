# Impact of AirBnB on Housing Crisis
After completing and submitting my assignment for Data Visualisation, I decided to revise my storytelling (mainly throwing out a tonne of graphs that are not important to story but are still available for exploration) and use updated datasets from AirBnB (updated the 29th December 2021).

This data is licensed under a Creative Commons Attribution 4.0 International License.

## Introduction
The aim of this project is tell a story about AirBnB listings through graphs in plotly package and dplyr packages in R.

Housing Crisis in Ireland is a hot topic at the moment, which is affecting vast number of people, both young and old. AirBnB is the leading short-term lease of a private property website, where individuals place their homes on AirBnB to lease it to tourists on a short-term basis.

In this report, I will be examining the impact of AirBnB on Irish Housing Crisis, by analysing AirBnB listings data by examining the RTZs from Residential Tenancies Board, Irish housing report from Daft.ie and the Homelessness Report from the Irish government.

## Background Understanding
### Housing Crisis
There is a huge housing crisis in Ireland, which has been defined as a shortage of affordable accommodation for renting or buying. Irish government has made attempts to reduce the housing crisis with plans of affordable and social housing, however, lobbyists criticise the government for late intervention and lack of innovative solutions. Both young adults (under 35 years old) and more older adults are worrying about not being able to afford a home because of rent prices and increasing house prices.

### Rent Report
Rent prices all over Ireland are increasing and Irish people worry about the affordability of rent, considering in areas like Dublin, individuals can pay up to 50% of their salary for rent. This is very nerve-wracking experience for the tenants. Daft.ie is the leading property website in Ireland, which publishes reports on the Irish housing market every quarter. For this next dataset, the report Q2 2021 was used to find out the rent in each town and city in Ireland (Lyons, 2021) .

### Rent Pressure Zones
To deal with rising rents and lack of affordable rental units, the government introduced Rent Pressure Zones (RPZs). These are areas located in parts of the country where rents are highest and rising, and where households have the greatest difficulty finding affordable accommodation (Residential Tenancies Board, 2021). Currently, there are six Local Authority Areas and 48 Local Electoral Areas (LEA) which have been designated as RTZs. In these areas, the rent cannot be increased by more than general inflation. The list is available to be viewed on Residential Tenancies Board (RTB) (Residential Tenancies Board, 2021).

### Homelessness
Due to the Irish rent prices, more and more individuals are loosing their homes and end up homeless on the streets. Some are homeless and are recoded in the data collected by the Irish government by Simon Community and Focus Ireland. However, there is a cohort of homeless people who live on couches of friends and families are not represented in the data. As the second quarter of 2021, there are over 4,000 adults homeless in Dublin. Homeless Report, which is published every month, captures homeless statistics (Department of Housing, Local Government and Heritage, 2021).

### AirBnB
AirBnB hosts and AirBnB, itself, have been strongly criticised for the increase of listings for short-term leasing for tourism. It has been reported that over 30,000 Irish listings on the site in Ireland for short-term lease (Pope, 2021). The article from The Irish Times continues to state that nearly half of those listings are rooms in private homes and over 10,000 entire homes are available all-year-round.

There have been talks of the Irish government to “bring legislation to create new measures that would target at least some of those properties and may see them return to the long-term rental market. Any moves which curtail the availability of AirBnB in popular tourism destinations around the country are likely to have a knock-on impact on accommodation availability and prices once international tourism resumes in a significant way in the post-pandemic period” (Pope, 2021). At the start of the pandemic, figures from estate agent Sherry FitzGerald show the number of properties available for rent in Dublin rose from 1,593 in November 2019 to 3,039 by the end March 2020 (Burke-Kennedy, 2021).

### Potential Long-Term Use of Accommodation Type at AirBnB

- Entire Rental Unit – this could be a house or an apartment. For this report, entire rental units will be viewed as a possible long-term accommodation for a family.
- Private Room – this is a private room in a shared house. This type of accommodation is usually used by students for the academic months of the year or young professionals (all year around).
- Shared Room – this is a shared room in a shared house. This type of accommodation is usually used by students for the academic months of the year.

## Research Question
- What is the impact of AirBnB on Irish Housing Crisis?
- Can moving entire rental units and private rooms from AirBnB listings take the pressure of the Irish Housing Crisis?

A lot of thought was brought to decided how to analyse and visualise the AirBnB data to answer the research questions above, so the following questions were developed as a lens to aid answering above questions.

- How many entire houses, private rooms and shared rooms are located in Pressure Rent Zones?
- How do AirBnB listings in RPZs compare to the rest of country on number of listings, room type, price, minimum nights, etc?
- When are these AirBnB listings available?
- How many entire houses in AirBnB listings, located in Pressure Rent Zones, are above 90-day threshold, requiring planning permission for the local authority?
- How many AirBnB listings are available for longer than short-term lease (14-days)?
- How many AirBnB listings, located in Pressure Rent Zones, target students?
- Which hosts own the most of AirBnB listings located in Pressure Rent Zones? How many listings are there? What is the average price, minimum stay, availability? What is the lease type and is it over the threshold?
- Should landlords rent their property or put it on AirBnB? Which is more profitable?
- What is the comparison between AirBnB listings and homeless figures?

## Data Preparation
The RMd report goes through how the treatment methods very extensively. It gives detailed description on how the datasets were combined. 
Here are the highlights:

Dropping
- outliers in price
- AirBnB Listings available between 23rd October 2021 and 21st October 2022.
- ‘Hotel room’ and 'Shared Room' from dataset

Creating new variables:
- Threshold: under-90 and over-90 days lease
- Planning permission: Required and Not Required
- Student Accommodation: True or False
- Rent or AirBnB: compares (available_nights by price) and (rent_per_month by 12)

## Data Visualisation

### Overview of AirBnB
![Picture1](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture1.png) 

It is clear from this graph that there are some parts of Ireland that have more AirBnB listings than others. It is easy to see that there are more properties available on the coast than inland.

![Picture2](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture2.png) 

![Picture3](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture3.png)

 Although, there is a difference between entire rental unit and private/shared room on price, there is no big difference between renting private/shared room inside or outside the RTZ. However, an entire rental unit is slightly more expensive in RTZs than outside RTZs. 

### Rent Pressure Zones
![Picture4](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture4.png) 

Map of Irelandpresents the density of AirBnB listings, highlighting the areas that are in RTZs (in red). Athough Dublin City, Cork City and Galway City are all in RTZs, it is possible to see the huge amount of AirBnB listings available, which can be affecting the Irish Housing Crisis.

| Room Type | RPZ Status | No of Listings | 
| :- | :- | :- |
| Entire rental unit | Non-RPZ | 8020 |
| Entire rental unit | RPZ | 3418 |
| Private room | Non-RPZ | 2967 |
| Private room | RPZ | 2855 |

There are more entire rental units and private rooms available outside of RTZs than there are in the RTZs.

![Picture5](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture5.png) 

Table above is summarised with this graph. There are more entire rental units and private rooms available outside of RTZs than there are in the RTZs. However, this could be due to fact that there are more houses in general outside the RTZs than inside the RTZs, which would show more AirBnB listings outside RTZs than inside RTZs.

![Picture6](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture6.png) 

Although, there is a difference between entire rental unit and private/shared room on price, there is no big difference between renting private/shared room inside or outside the RTZ. However, an entire rental unit is slightly more expensive in RTZs than outside RTZs.


### Entire Rental Units
A new dataset was created where AirBnB listings were selected that offered entire rental unit. This new dataset was used for this section of the report.

![Picture7](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture7.png)  

Kerry and Donegal have more entire rental units than other counties. Dublin is only 5th highest, while Cork and Galway are in 3rd and 4th place.

![Picture7_1](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture7_1.png)  

When Kerry was examined, 314 AirBnB listings are in the RTZ, while the rest is outside the RTZ. Both County Galway and County Cork have AirBnB listings in RTZ and outside of it. All Dublin City AirBnBlistings, Cork City AirBnB listings and Galway City AirBnB listings is in the RTZ.

![Picture8](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture8.png) 

It is visible that a lot of properties are not available all year around. Unfortunately, no reason is provided why the property is unavailable.

![Picture9](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture9.png) 

The table above the shows the breakdown of which entire rental units should be rented out or leased out as AirBnB, when only the daily price and daily rent rate is to be considered.

![Picture10](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture10.png)  

However, when comparing total potential income (available nights by price) and annual income (rent_in_ireland.csv by 12), it seems that most landlords are missing out on the potential annual rent. THis could be due to the fact that the rental unit is not available all year around.

##### Planning Permission
![Picture11](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture11.png) 

There are very small amount of properties in the Rent Pressures Zones that are over 90 day threshold that would require planning permission.

| RPZ Status | RPZ Status | Planning Permission | 
| :- | :- | :- |
| Non-RPZ | over-90 | Not Required | 
| Non-RPZ | under-90 | Not Required |	
| RPZ | over-90 | Planning Required |	
| RPZ |under-90 | Not Required |

Homeowners in RTZs are required to apply for planning permission if they let out their entire home (principal private residence) for short-term lets of more than 90 days in total while they are away. Principal private residence is the place where one ordinarily live.
There are 2350 properties in the Rent Pressures Zones that are over 90 day threshold that would require planning permission.

### Private Rooms
TBC




## Reference
Burke, C. (2021) Rents continue to rise across Ireland as number of rental homes available hits ‘all-time low’, TheJournal.ie. Available at: https://www.thejournal.ie/daft-rental-report-all-time-low-5596453-Nov2021/ (Accessed: 17 December 2021).

Burke-Kennedy, E. (2021) Airbnb exodus increases stock of rental property in Dublin by 90%, The Irish Times. Available at: https://www.irishtimes.com/business/economy/airbnb-exodus-increases-stock-of-rental-property-in-dublin-by-90-1.4654155 (Accessed: 17 December 2021).

Citizensinformation.ie (no date) Renting your property for short-term lets. Citizensinformation.ie. Available at: https://www.citizensinformation.ie/en/housing/owning_a_home/home_owners/renting_your_property_for_shortterm_lets.html (Accessed: 17 December 2021).

Department of Housing, Local Government and Heritage (2021) Homeless Report - September 2021. Available at: https://www.gov.ie/en/publication/0d7a7-homeless-report-september-2021/ (Accessed: 19 December 2021).

Lyons, R. (2021) Irish Rental Report Q2 2021. Available at: https://ww1.daft.ie/report/ronan-lyons-2021q2-daftrentalprice?d_rd=1 (Accessed: 17 December 2021).

McGrath, D. (2021) Number of homeless people in Ireland rises for third month in a row – 8,212 adults and children now without home, Independent. Available at: https://www.independent.ie/irish-news/number-of-homeless-people-in-ireland-rises-for-third-month-in-a-row-8212-adults-and-children-now-without-home-40885752.html (Accessed: 19 December 2021).

Pope, C. (2021) New restrictions likely to reduce supply of short-term rental property, The Irish Times. Available at: https://www.irishtimes.com/business/new-restrictions-likely-to-reduce-supply-of-short-term-rental-property-1.4653404 (Accessed: 17 December 2021).

Residential Tenancies Board (2021) What are Rent Pressure Zones (RPZ)? Available at: https://www.rtb.ie/during-a-tenancy/rent-review-in-a-rent-pressure-zone-rpz?gclid=Cj0KCQiAzfuNBhCGARIsAD1nu-8YhjJPsVbhgWjuM0et4lZX2ansT4b4XkLEEx9G63vDiVsptSzv8toaAkdDEALw_wcB (Accessed: 19 December 2021).