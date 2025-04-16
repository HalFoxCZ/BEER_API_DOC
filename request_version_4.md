# DOC for requesting this API through CURL request:

[Back](README.md) to README.md

Here is step by step tutorial for using this API for it's version 4 and lower.

This tutorial covers fetching request to info endpoint with requesting server info.

( `https://bohmda22.sps-prosek.cz/__BEERAPI__/API/v1/info.php`  - [Doc](Info.md))

1. First you need to choose an endpoint you want to request (DUH no shit sherlock)
2. Then you have to setup your url (I recomend to setup it from this pattern soo it will be easier to update, and can be fetched from DB for updates, etc...) :
```
$api = "https://bohmda22.sps-prosek.cz/__BEERAPI__/API/"; // base API url, will be still this same
$version = "v4"; // version you want to use
$endpoint = "info.php"; // endpoint name

// create the finall url for request
$url = $api . $version . "/" . $endpoint;
```
3. After you have the API request url, you have to setup the curl request:
```
curl_setopt($crl, CURLOPT_RETURNTRANSFER, true);
curl_setopt($crl, CURLINFO_HEADER_OUT, true);
curl_setopt($crl, CURLOPT_POST, true);
curl_setopt($crl, CURLOPT_POSTFIELDS, array(
    "user"=> YOUR_USER_ID, // replace with your own user ID 
    "auth"=> YOUR_REQUEST_AUTH, // replace with your own auth token
    "request"=> SERVER_INFO // set up what request you want
));
```
4. Execute curl, and close connection
```
$return = curl_exec($crl);

curl_close($crl);
```
5. Optional - Use json_decode to get usable php array:
```
$php_array = json_decode($return, true);

```
