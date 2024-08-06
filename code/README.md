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

## Data Sources

Lyons, R. (2024) *Irish Rental Report Q1 2024.* Available at: https://ww1.daft.ie/report/ronan-lyons-2021q2-daftrentalprice?d_rd=1 (Accessed: 28th June 2024).

Residential Tenancies Board (2024) *What are Rent Pressure Zones (RPZ)?* Available at: https://www.rtb.ie/registration-and-compliance/setting-and-reviewing-rent/guide-to-rent-pressure-zones (Accessed: 31 July 2024).


 

# References
Burke, C. (2021) *Rents continue to rise across Ireland as number of rental homes available hits ‘all-time low’, TheJournal.ie.* Available at: https://www.thejournal.ie/daft-rental-report-all-time-low-5596453-Nov2021/ (Accessed: 17 December 2021).

Burke-Kennedy, E. (2021) *Airbnb exodus increases stock of rental property in Dublin by 90%, The Irish Times.* Available at: https://www.irishtimes.com/business/economy/airbnb-exodus-increases-stock-of-rental-property-in-dublin-by-90-1.4654155 (Accessed: 17 December 2021).

Citizensinformation.ie (no date) *Renting your property for short-term lets.* Citizensinformation.ie. Available at: https://www.citizensinformation.ie/en/housing/owning_a_home/home_owners/renting_your_property_for_shortterm_lets.html (Accessed: 17 December 2021).

Pope, C. (2021) *New restrictions likely to reduce supply of short-term rental property, The Irish Times.* Available at: https://www.irishtimes.com/business/new-restrictions-likely-to-reduce-supply-of-short-term-rental-property-1.4653404 (Accessed: 17 December 2021).


