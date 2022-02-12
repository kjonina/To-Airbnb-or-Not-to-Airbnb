# Karina.Jonina.Project
R Project for Data Visualisation (MSc Module)


## Introduction
The aim of this project is tell a story about AirBnB listings through graphs in plotly package and dplyr packages in R.

Housing Crisis in Ireland is a hot topic at the moment, which is affecting vast number of people, both young and old. AirBnB is the leading short-term lease of a private property website, where individuals place their homes on AirBnB to lease it to tourists on a short-term basis.

In this report, I will be examining the impact of AirBnB on Irish Housing Crisis, by analysing AirBnB listings data by examining the RTZs from Residential Tenancies Board, Irish housing report from Daft.ie and the Homelessness Report from the Irish government.

## Business Understanding
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

###  Potential Long-Term Use of Accommodation Type at AirBnB

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
- Rent or AirBnB: compares (available_nights ny price) and (rent_per_month by 12)


## Data Visualisation

### Overview of AirBnB
![Picture1](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture1.png) 

![Picture2](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture2.png) 

![Picture3](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture3.png) 

![Picture4](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture4.png) 

![Picture5](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture5.png) 

![Picture6](https://github.com/kjonina/airbnb_and_irish_housing_crisis/blob/main/graphs/Picture6.png) 

