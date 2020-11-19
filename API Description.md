
## Manitoba Covid Tracker API

#### API Description: The Manitoba Covid Tracker API can be used to programmatically retrieve and analyze data relate to the current Covid situation in the Manitoba province.


https://dog.ceo/dog-api/documentation/


Cases
Deaths
Recoveries

 
Manitoba covid case breakdown by health region
##### Options: 

* GET method 1: get all covid case recoveries in Manitoba. parameters: health regions (***optional***), time (dd.mm.yyyy) (***optional***)

* GET method 2: get covid case breakdown by health regions. parameters: health regions

* GET method 3: get covid deaths and hospitalizations. parameters: health regions

#### Sample Request
###### Get Recovery
```
https://api.covidmanitoba.ca/recovery/json?region=bisonnorth&time=30.08.2020
```
