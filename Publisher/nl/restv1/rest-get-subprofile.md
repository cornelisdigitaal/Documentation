# REST API: GET subprofile

Waarschuwing: Je bekijkt nu het overzicht voor de oude versie van onze 
API. Wij raden aan om [versie 2](../restv2/rest-api.md) van de API te gebruiken.

Als je alle gegevens van een enkel subprofiel wilt opvragen, dan kun je die
opvragen door middel van een eenvoudige HTTP GET call naar de volgende URL

`https://api.copernica.com/v1/subprofile/$id?access_token=xxxx`

De code **$id** moet je vervangen door de numerieke identifier van het subprofiel
dat je opvraagt.


## Geretourneerde velden

De methode retourneert gegevens van een subprofiel. De volgende eigenschappen 
worden teruggegeven:

* **ID**: numeriek ID van het profiel
* **profile**: numeriek ID van het profiel waar het subprofiel onder hoort
* **collection**: ID van de collectie waarin het profiel is opgeslagen
* **secret**: de "geheime" code die aan een profiel is gekoppeld
* **created**: tijdstip waarop het profiel in aangemaakt, in YYYY-MM-DD hh:mm:ss formaat
* **modified**: tijdstip waarop het profiel voor het laatst is bijgewerkt, in YYYY-MM-DD hh:mm:ss formaat
* **fields**: associative array / object van veldnamen en veldwaardes
* **interests**: array van de interesses van het profiel


## Voorbeeld in PHP

Het volgende PHP script demonstreert hoe je de API methode kunt aanroepen.

```php
// vereiste scripts
require_once('copernica_rest_api.php');

// verander dit naar je access token
$api = new CopernicaRestApi("your-access-token");

// voer de methode uit en print het resultaat
print_r($api->get("profile/1234"));
```

Dit voorbeeld vereist de [REST API class](rest-php).

    
## Meer informatie

* [Overzicht van alle API calls](rest-api)
* [Opvragen van profiel ID's](rest-get-database-subprofileids)
* [Profiel toevoegen aan een database](rest-post-profile-subprofiles)
* [Profiel bijwerken](rest-put-subprofile-fields)
* [Profiel verwijderen](rest-delete-subprofile)
