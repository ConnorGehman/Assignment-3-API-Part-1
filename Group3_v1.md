## Manitoba Covid Tracker API

#### Description  
The Manitoba Covid Tracker API provides a summary of covid cases, recoveries, deaths, and hospitalization across the province.
 
#### Endpoints: (all GET requests)
##### Get all Covid cases in Manitoba  
This endpoint will retrieve all covid cases from a requested health region within a specified date range. If no regions or dates are requested, it will retrieve all recorded covid cases in Manitoba up to the current date. 
- Parameters: 
  - **region** (string): health regions (***optional***)
  - **fromdate** (string): from date (dd.mm.yyyy) (***optional***)
  - **todate** (string): to date (dd.mm.yyyy) (***optional***)
- Sample Request: 
  ```
  https://api.covidmanitoba.ca/cases/json?region=winnipeg&fromdate=18.11.2020&todate=19.11.2020
  ```
- Sample Response: 
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
  
  
##### Get all Covid case recoveries in Manitoba  
This endpoint will retrieve all covid case recovieries from a requested health region at a specified date. If no regions or dates are requested, it will retrieve all recorded covid cases in Manitoba up to the current date.
- Parameters: 
  - **region** (string): health regions (***optional***)
  - **todate** (string): to date (dd.mm.yyyy) (***optional***)
- Sample Request:
  ```
  https://api.covidmanitoba.ca/recoveries/json?region=all&todate=30.08.2020
  ```
- Sample Response: 
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
  

##### Get Covid deaths and hospitalizations  
This endpoint will retrieve all deaths and hospitalizations caused by Covid from the requested health region. If no region is selected, all regions in Manitoba will be returned.
- Parameters: 
  - **region** (string): health regions
- Sample Request: 
  ```
  https://api.covidmanitoba.ca/deathsandhospitalizations/json?region=winnipeg
  ```
- Sample Response:
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
