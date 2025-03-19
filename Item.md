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


## Returned JSON:


### Scope - Default
```
 "headers": "Content-Type: application/json; charset=utf-8",
    "url": "/__BEERAPI__/API/v3/item.php",
    "args": {
        "ID": 5,
        "scope": "Default"
    },
    "data": [
        {
            "brewery_name": "Caldera Brewing Company",
            "review_profilename": "djeucalyptus",
            "review_overall": "4.5",
            "beer_style": "Rauchbier",
            "beer_name": "Rauch Ür Bock"
        }
    ],
    "time": 0
}
```

### Scope - Extended
```
{
    "headers": "Content-Type: application/json; charset=utf-8",
    "url": "/__BEERAPI__/API/v3/item.php",
    "args": {
        "ID": 5,
        "scope": "Extended"
    },
    "data": [
        {
            "ID": "5",
            "brewery_id": "1075",
            "brewery_name": "Caldera Brewing Company",
            "review_profilename": "djeucalyptus",
            "review_overall": "4.5",
            "beer_style": "Rauchbier",
            "beer_abv": "7.4",
            "beer_id": "58046",
            "beer_name": "Rauch Ür Bock"
        }
    ],
    "time": 0
}

```

### Scope - Full
```
{
    "headers": "Content-Type: application/json; charset=utf-8",
    "url": "/__BEERAPI__/API/v3/item.php",
    "args": {
        "ID": 5,
        "scope": "Full"
    },
    "data": [
        {
            "ID": "5",
            "brewery_id": "1075",
            "brewery_name": "Caldera Brewing Company",
            "review_time": "1300936020",
            "review_overall": "4.5",
            "review_aroma": "4.0",
            "review_appearance": "4.0",
            "review_profilename": "djeucalyptus",
            "beer_style": "Rauchbier",
            "review_palate": "4.0",
            "review_taste": "4.5",
            "beer_name": "Rauch Ür Bock",
            "beer_abv": "7.4",
            "beer_beerid": "58046"
        }
    ],
    "time": 0
}

```
