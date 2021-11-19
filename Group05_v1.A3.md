# comp_3040_a3_group5

## API Description  
Our API offers real time weather information for locations within Manitoba. Given a location name, you can access temperature, precipitation, sunrise and sunset times.

## List of Endpoints with Parameters  
 1. Temperature:  
 ```https://winterpeg.com/temperature/{cityName}/{datetime}/```
 2. Precipitation:  
 ```https://winterpeg.com/precipitation/{cityName}/{datetime}/```
 3.  Sunrise and sunset time:  
 ```https://winterpeg.com/sunrise-sunset/{cityName}/{date}/```
 ### Parameters:
  - cityName: Name of the city that you want to get information from (type: String)
  - datetime: YYYY-MM-DD::HH:MM:SS format (type: String)
  - date: YYYY-MM-DD format (type: String)
## Description of Resources (formatted as JSON)  

## Sample Request with Sample Response  
