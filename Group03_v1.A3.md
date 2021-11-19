# Manitoba Population Group 3 API
We are offering a basic API which will provide polulations of towns and cities in Manitoba for a given **area** and **time period**.

## API Documentation
Our API works with a simple **GET** request to https://api.mbpopulation.org/json.

## Parameters
* Location (string) - Name of town/city. Required.
* Year (integer) - Year in YYYY format. Required.
* Month (integer) - Month in MM format. If not present, month will default to ```1``` (January). Optional.

## Resources
* Population (integer) - Population of town/city
* Area (integer) - Total area of the location in km^2
* Population Density (integer) - population / area

## Sample Requests and response
### Response without specific month:
Sample request:
```
https://api.mbpopulation.org/json?location=winnipeg&year=2016
```

Response

```
{
      "results":
      {
	“location”:"Winnipeg",
	“year”: 2016,
	“month”: 1,
	“population”:705244,
	“area”: 464.33,
	“population_density” : 1518.8,
      },
       "status":"OK"
}
```

### Response with specific month (month = 12):
Sample request:
``` 
https://api.mbpopulation.org/json?location=winnipeg&year=1999&month=12 
```

Response

```
{
      "results":
      {
       	“location”:"Winnipeg",
	“year”: 1999,
	“month”: 12,
	“population”:673000,
	“area”: 464.33,
	“population_density” : 1449.4,
      },
      "status":"OK"
}
```

## Usage limits and attribution
The Manitoba Population Group 3 API can be used free of charge. 

## Credits
- https://www.worldatlas.com/articles/the-10-biggest-cities-in-manitoba.html
- https://sunrise-sunset.org/api
- https://www.macrotrends.net/cities/20407/winnipeg/population 
- https://datacommons.org/ranking/Count_Person/City/wikidataId/Q1948?h=wikidataId%2FQ6465074
