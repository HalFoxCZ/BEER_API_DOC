# BEER_API_DOC
Documentation for my BEER_API
##
Working request URI:
> https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/info.php  - [Doc](Info.md)

In progress:
> https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/items.php  - [Doc](Items.md)
> 
> https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/item.php  - [Doc](Item.md)

## Paramters for request:
|Paramter | Info                            | Comment           |
|---------|---------------------------------|-------------------|
| user    | Value of your user ID           | For testing: 1    |
| auth    | Your api key                    | For testing: YYXD |
| request | Name of request you want to get |                   |
| table   | For table specific request      |                   |
## Allowed request:
| Request name | Server answer                                             |
|--------------|-----------------------------------------------------------|
| SERVER_INFO  | Returns time of server, its timezone and used memory      |
| TABLE_COUNT  | Returns number of tables in database                      |
| TABLE_ROWS   | Returns number of rows in table. Must specifie table name |
| TABLE_LIST   | Returns list of tables in database                        |  

