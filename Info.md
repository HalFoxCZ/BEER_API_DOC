# Doc for Info endpoint:


> https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/info.php

All request to this endpoint <b>MUST</b> be a post requests

Paramters under dashed line doesnt need to be included in specific request
if they are not required by the request itself (must include it for 
<b>TABLE_ROWS</b> request, ect...)

## Paramters for request:
|Paramter | Info                            | Comment           |  Datatype          |
|---------|---------------------------------|-------------------|--------------------|
| user    | Value of your user ID           | For testing: 1    |  Int               |
| auth    | Your api key                    | For testing: YYXD |  String            |
| request | Name of request you want to get |                   |  String            |
|---------|---------------------------------|-------------------|--------------------|
| table   | For table specific request      | <b>Not required</b>|  String           |

## Allowed request:
| Request name | Server answer                                             |
|--------------|-----------------------------------------------------------|
| SERVER_INFO  | Returns time of server, its timezone and used memory      |
| TABLE_COUNT  | Returns number of tables in database                      |
| TABLE_ROWS   | Returns number of rows in table. Must specifie table name |
| TABLE_LIST   | Returns list of tables in database                        |  
