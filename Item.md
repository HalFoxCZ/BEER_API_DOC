# Doc for Item endpoint:

[Back](README.md) to README.md

> Endpoint : https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v3/item.php


This ednpoint returns array of all info about specified item

All request to this endpoint <b>MUST</b> be via post request


Paramters under dashed line doesnt need to be included on this endpoint, but its recomended to include them even though they have default values set. Bold values are default.


## Pamaters:

|Parametr | Info | Comment | Datatype|
|-|-|-|-|
| user    | Value of your user ID           | For testing: 1    |  Int               |
| auth    | Your api key                    | For testing: YYXD |  String            |
|ID| ID of item you want to recieve info about | You can get ID from the <b>[Items](Items.md)</b> endpoint  | Int |
|----------|--------------------------------------------|---------------------------------------------|------------------|----------|
|Scope| How much information you  want to get |Values: <b>Default</b>, Extended, Full | String |
