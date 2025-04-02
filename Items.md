# Doc for Items endpoint:

[Back](README.md) to README.md

> Endpoint : `https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v3/items.php`


This endpoint returns array of items from DB

All request <b>MUST</b> be via POST request

Paramters under dashed line doesnt need to be included on this endpoint, but its recomended to include them even though they have default values set. Bold values are default.

## Default values:
> Page : 1
> 
> Limit : 10
> 
> Sort : ASC
> 
> Order: id


## Paramters:

| Paramter | Ifno | Comment | Datatype |
|---------|------|----------|-----------|
| user    | Value of your user ID           | For testing: 1    |  Int               |
| auth    | Your api key                    | For testing: YYXD |  String            |
|---------|--------------------------------------------|--------------------------------|--------------------|
| Page     |Number of page you want | | Int|
| Limit | Number of items per page | Max value 50 (<b>10</b>)| Int |
|Sort | What order you want items to be |Values: <b>ASC</b>, DESC| String |
|Order| By what value to order items |Values: <b>id</b>, name, date| String |


## Return JSON

#### page_count is only returned in version 4 and higher. it is calculated based on limit set and total items in database.
```
{
    "headers": "Content-Type: application/json; charset=utf-8",
    "url": "/__BEERAPI__/API/v4/items.php",
    "args": {
        "page": 5,
        "limit": 5,
        "sort": "ASC",
        "order": "id",
        "page_count": 49
    },
    "data": [
        {
            "ID": 21,
            "name": "Caldera Pale Ale",
            "rating": 5.5
        },
        {
            "ID": 22,
            "name": "Caldera Pale Ale",
            "rating": 5.5
        },
        {
            "ID": 23,
            "name": "Pilot Rock Porter",
            "rating": 5.8
        },
        {
            "ID": 24,
            "name": "Vas Deferens Ale",
            "rating": 8.1
        },
        {
            "ID": 25,
            "name": "Vas Deferens Ale",
            "rating": 8.1
        }
    ],
    "time": 0
}
```
