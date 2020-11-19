## Manitoba Covid Tracker API

#### Description  
The Manitoba Covid Tracker API can be used to programmatically retrieve and analyze data related to the current Covid situation in the province of Manitoba.

 
Manitoba covid case breakdown by health region
#### Endpoints: (all GET requests)
##### Get all Covid case recoveries in Manitoba  
- Parameters: 
  - **region** (string): health regions (***optional***)
  - **todate** (string): to date (dd.mm.yyyy) (***optional***)

##### Get all Covid cases in Manitoba  
- Parameters: 
  - **fromdate** (string): from date (dd.mm.yyyy) (***optional***)
  - **todate** (string): to date (dd.mm.yyyy) (***optional***)

##### Get Covid deaths and hospitalizations  
- Parameters: 
  - **region** (string): health regions


#### Sample Requests

###### Get Recoveries

```
https://api.covidmanitoba.ca/recoveries/json?region=all&todate=30.08.2020
```

###### Get Covid Cases

```
https://api.covidmanitoba.ca/cases/json?region=winnipeg&fromdate=18.11.2020&todate=19.11.2020
```

###### Get Deaths and Hospitalizations

```
https://api.covidmanitoba.ca/deathsandhospitalizations/json?region=winnipeg
```

#### Sample Response

###### Get Recoveries

```
    {
      "results":
      {
        "Health Region": "All",
        "Recovered":"89,232",
        "To date":"August 30th, 2020"
      },
       "status":"success"
    }
```

###### Get Covid Cases

```
    {
      "results":
      {
        "Health Region": "Winnipeg",
        "Covid Cases":"271",
        "From date":"November 18th, 2020",
        "To date":"November 19th, 2020"
      },
       "status":"success"
    }
```

###### Get Deaths and Hospitalizations

```
    {
      "results":
      {
        "Health Region": "Winnipeg",
        "Death":"142",
        "Hospitalizations":"160",
      },
       "status":"success"
    }
```
