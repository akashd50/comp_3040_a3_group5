# Winterpeg (Manitoba Weather API)

## API Description  
Our API provides real time weather information for any named location within the Canadian province of Manitoba. With simply a city or town name, the user will receive corresponding temperature, precipitation, and even sunrise and sunset times.

## List of Endpoints with Parameters  
1. Get /temperature  
```https://winterpeg.com/temperature?location={location_name_string}&date={date_string}&time={time_string}```  
Get the temperature in Celsius at provided location.

2. Get /precipitation  
```https://winterpeg.com/precipitation?location={location_name_string}&date={date_string}&time={time_string}```  
Get precipitation amounts in mm at provided location.

3. Get /sunrisesunset  
```https://winterpeg.com/sunrisesunset?location={location_name_string}&date={date_string}```  
Get sunrise and sunset times in UTC-6 unadjusted for Daylight Savings Time (DST) at provided location.

#### Parameters
- location: name of the city or town for which the user wishes to obtain weather information
- date: YYYY-MM-DD format (type: String)
- time: HH:MM:SS format (type: String)


## Description of Resources  
*formatted as JSON*  

1. Temperature:
```
{
 "temperature": Measured at ground level in Celsius,
 "wind-speed": Measured at 2 metres above ground level in km/h,
 "wind-chill": Measured at 2 metres above ground level in Celsius
}
```

2. Precipitation:
```
{
 "rainfall": Accumulated measurement in the previous 12 hours in mm,
 "snowfall": Accumulated measurement in the previous 12 hours in mm,
 "humidity": Prevailing measurement in percentage (0-100)
}
```

3. Sunrise and Sunset:
```
{
"sunrise": Daily UTC-6 unadjusted for DST in 24 hour HH:MM format,
"sunset": Daily UTC-6 unadjusted for DST in 24 hour HH:MM format
}
```

## Sample Request with Sample Response  

#### Request
1. Temperature:  
```https://winterpeg.com/temperature?location=Winnipeg&date=1925-09-12&time=15:09:29```  

2. Precipitation:  
```https://winterpeg.com/precipitation?location=Brandon&date=2001-09-11&time=08:10:59```  

3. Sunrise and sunset time:  
```https://winterpeg.com/sunrisesunset?location=Gimli&date=2020-03-13```  

#### Response
1. Temperature:
```
{
 "temperature": "-50 C",
 "wind-speed": "5 km/h",
 "wind-chill": "-55 C"
}
```

2. Precipitation:
```
{
 "rainfall": "0 mm",
 "snowfall": "2 mm",
 "humidity": "15%"
}
```

3. Sunrise and Sunset:
```
{
"sunrise": "07:27",
"sunset": "18:45"
}
```
