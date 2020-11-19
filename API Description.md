
## Manitoba Covid Tracker API

#### description : The Manitoba Covid Tracker API can be used to programmatically retrieve and analyze data relate to the current Covid situation in the Manitoba province.


https://dog.ceo/dog-api/documentation/


Cases
Deaths
Recoveries

 
Manitoba covid case breakdown by health region
##### Options: 

* GET Recovery: get all covid case recoveries in Manitoba. parameters: health regions (***optional***), date (dd.mm.yyyy) (***optional***)

* GET Breakout: get covid case breakdown by health regions. parameters: health regions

* GET method 3: get covid deaths and hospitalizations. parameters: health regions


###### Get Recovery

***Request***:
```
https://api.covidmanitoba.ca/recovery/json?region=bisonnorth&date=30.08.2020
```

***Response***
```
    {
      "results":
      {
        "date":"August 30th, 2020",
        "Total cases:":"123,858",
        "Recovered":"89,232",
      },
       "status":"success"
    }
  ```


