# Doc for Items endpoint:

[Back](README.md) to README.md

> Endpoint : https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v3/items.php


This endpoint returns array of items from DB

All request <b>MUST</b> be via POST request

Paramters under dashed line doesnt need to be included on this endpoint, but its recomended to include them even though they have default values set. 


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
| Limit | Number of items per page | Max value 50 | Int |
|Sort | What order you want items to be |Values: ASC, DESC| String |
|Order| By what value to order items |Values: id, name, date| String |
