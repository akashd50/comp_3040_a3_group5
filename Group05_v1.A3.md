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
### Sample Request
1. Temperature:  
 ```https://winterpeg.com/temperature?cityName=Winnipeg&datetime=1925-09-12::15:09:29```
2. Precipitation:  
 ```https://winterpeg.com/temperature?cityName=Winnipeg&datetime=1925-09-12::15:09:29```
3.  Sunrise and sunset time:  
 ```https://winterpeg.com/sunrise-sunset?cityName=Winnipeg&date=1999-09-09```
### Sample Response
1. Temperature:
```
{
 "temperature": "-1 C",
 "wind-speed": "30 mph",
 "wind-chill": "56 C"
}
```
2. Precipitation:
```
{
 "precipitation": "5 mm",
 "rainfall": "2 mm",
 "snowfall": "8 mm",
 "humidity": "90%"
}
```
3. Sunrise and sunset time:
```
{
"sunrise": "7:27:02",
"sunset": "17:05:55"
}
```
