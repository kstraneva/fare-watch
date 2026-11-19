# fare-watch
WhatsApp alerts for cheap weekend flights from NYC to see family (SLC, PHX, AUS, LAX, RNO, SEA)

## Data Source 
SerpApi's Google Flights API scrapes flight results from Google flights. You pass in departure aiport(s), destionation aiport code, and dates and it returns the results as a JSON object. 

SerpApi has an API limit of 250 free requests per month. In the interest of not paying for another subscription, I will stick below that limit and run this search weekly. 

## Restrictions

Possible Destinations: SLC, PHX, RNO, AUS, LAX, SEA. 

Preferred carriers: Delta, Southwest, United, JetBlue. 

Stops and Travel Time: Nonstop preferred and 1 stop is tolerated if saves more than $100. Total travel time (including layover) for 1 stop trips should be less than 10 hours. 

Timing: The cheapest flight occurs at different timep per season per (source) 

Winter
Spring
Summer
Fall







## Scheduler 

A Github Actons Chron Job will be used to run this job. 

## Alerts 

CallMeBot on WhatsApp will be used to receive alerts as messages. 


