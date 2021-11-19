# Group 3 Comp 3040 API
We are offering a basic API which will provide polulations of towns and cities in Manitoba for a given **area** and **time period**.

## API Documentation
Our API works with a simple **GET** request to https://api.mbpopulation.org/json.

## Parameters
* Area (String) - Name of town/city. Required
* TimePeriod (Integer) - Year in XXXX format. Required

## Resources

## Sample Requests and response
### Response without specific month
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

### Response with specific month
Sample request (month = 12)
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
