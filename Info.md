# Doc forInfo endpoint:


> https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/info.php

All request to this endpoint <b>MUST</b> be a post requests


## Paramters for request:
|Paramter | Info                            | Comment           |
|---------|---------------------------------|-------------------|
| user    | Value of your user ID           | For testing: 1    |
| auth    | Your api key                    | For testing: YYXD |
| request | Name of request you want to get |                   |
|---------|---------------------------------|-------------------|

| table   | For table specific request      | <b>Not required</b>|

## Allowed request:
| Request name | Server answer                                             |
|--------------|-----------------------------------------------------------|
| SERVER_INFO  | Returns time of server, its timezone and used memory      |
| TABLE_COUNT  | Returns number of tables in database                      |
| TABLE_ROWS   | Returns number of rows in table. Must specifie table name |
| TABLE_LIST   | Returns list of tables in database                        |  
