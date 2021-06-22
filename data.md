## Data

As mentioned in section Introduction, how to select a right neighborhood in Toronto to open a Sushi restaurant becomes an important business problem. In order to address this problem, we can employ a data-driven approach. Many other North-American cities, for exmaple, New York City, has already had Sushi restaurants. We can compare Toronto's neighborhoods with their counterparts in New York City. First, we can select neighborhoods in New York City in which Sushi restaurants became popular. Second, we can find similar neighborhoods in Toronto as those selected New York City neighborhoods other than Sushi restaurants. The resulting neighborhoods could be potential candidates for a Sushi restaurant.

### Neighborhoods data

For Toronto, we can retrieve its neighborhoods data via wikipedia (https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M).
It will contain neighborhoods and their geographical information, such as latitude	and longitude.
See data sample below:

| PostalCode |	Borough |	Neighborhood |	Latitude |	Longitude |
|------------|----------|-------------|-----------|------------|
| M3A	|    North York	| Parkwoods	| 43.7532586 | -79.3296565 |
| M4A	| North York	| Victoria Village |	43.7258823	| -79.3155716 |
| M5A	| Downtown Toronto |	Regent Park, Harbourfront	| 43.6542599	| -79.3606359

For New York City, we can get data from IBM Developer Skills Network (https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DS0701EN-SkillsNetwork/labs/newyork_data.json). It will contain neighborhoods and their geographical information too.

### Foursquare data

AS long as neighorhoods' geographical information is available, we can further explore each neighborhood via Foursquare API. This API will return what venues are located in each neighborhood, such as parks, gyms and cafés.
Based on the venue data, we can then do clustering so that we can find which Toronto neighborhoods share the common venue patterns with their counterparts in New York City.