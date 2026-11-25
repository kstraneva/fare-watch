# fare-watch
WhatsApp alerts for cheap weekend flights from NYC to see family (SLC, PHX, AUS, LAX, RNO, SEA)

## Data Source 
SerpApi's Google Flights API scrapes flight results from Google flights. You pass in departure airport(s), destination airport code, and dates and it returns the results as a JSON object. 

SerpApi has an API limit of 250 free requests per month. In the interest of not paying for another subscription, I will stick below that limit and run this search weekly. 

## Restrictions

Possible Destinations: SLC, PHX, RNO, AUS, LAX, SEA. 

Travel Dates: Weekend trips departing Thursday, returning either Sunday (Thu→Sun) or Tuesday (Thu→Tue).

Preferred carriers: Delta, Southwest, United, JetBlue. 

Stops and Travel Time: Nonstop preferred and 1 stop is tolerated if it saves more than $100. Total travel time (including layover) for 1 stop trips should be less than 10 hours. 

Timing: Domestic fares are cheapest at different times depending on the season according to [CheapAir's 2024 Airfare Study](https://prnewswire.com/news-releases/annual-airfare-study-by-cheapaircom-unveils-top-tips-for-saving-on-2024-domestic-flights-302047596.html)

| Season | Travel months | Best time to buy | fare-watch search window |
|---|---|---|---|
| Winter | Dec–Feb | ~42 days out | 4–7 weeks out |
| Spring | Mar–May | ~44 days out | 4–7 weeks out |
| Summer | Jun–Aug | ~35 days out | 4–7 weeks out |
| Fall | Sep–Nov | ~55 days out | 5–8 weeks out |

Across all domestic flights, [Google Flights reports](https://blog.google/products-and-platforms/products/search/holiday-travel-trends-2026/) that prices are lowest ~39 days before departure, with a low-price window of 22-57 days. 

## Scheduler 

A Github Actons cron job will be used to run this job every Thursday.

## Alerts 

CallMeBot on WhatsApp will be used to receive alerts as messages. 

Alert rules:
- Every Thursday, one WhatsApp message lists all trips under $400 that meet the restrictions above.
- Trips under $300 are flagged at the top of the message.
- If nothing qualifies, no message is sent.

## Status: 

Waiting for the CallMeBot to reopen to send messages... CallMeBot.com