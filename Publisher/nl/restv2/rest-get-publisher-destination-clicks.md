# REST API: GET clicks (Publisher destination)

Net zoals je van een mailing statistieken op kunt vragen kun je ook de statistieken 
per emailing destination opvragen. Je kan deze opvragen met een 
HTTP GET call naar de volgende URL:

`https://api.copernica.com/v2/publisher/destination/$id/clicks?access_token=xxxx`

Hier moet `$id` vervangen worden door de ID van de mailing destination. Deze methode 
ondersteunt ook het gebruik van de [fields parameter](./rest-fields-parameter) 
voor het **timestamp** veld.

## Teruggegeven velden

Deze methode geeft een JSON object terug met clicks. Voor elke click 
is de volgende informatie beschikbaar:

* **ID**: ID van de click.
* **link_id**: ID van de geklikte link.
* **link**: De geklikte link.
* **link_title**: Titel van de geklikte link.
* **timestamp**: Tijdstempel van de click.
* **ip**: De IP waar de click vandaan kwam.
* **user-agent**: De user agent string van de clicker.
* **referer**: De referer van de clicker.
* **emailing**: De ID van de emailing waar de click vandaan kwam.
* **destination**: De destination waar de click vandaan kwam.
* **profile**: De ID van het profiel waar de click vandaan kwam.
* **subprofile**: De ID van het subprofiel waar de click vandaan kwam (als deze beschikbaar is).

## PHP voorbeeld

Dit script demonstreert hoe je de API methode kunt gebruiken:

```php
// vereiste scripts
require_once('copernica_rest_api.php');

// verander dit naar je access token 
$api = new CopernicaRestAPI("your-access-token", 2);

// voer het verzoek uit
print_r($api->get("publisher/destination/{$destinationID}/clicks/"));
```

Dit voorbeeld vereist de [REST API klasse](./rest-php).

## Meer informatie

* [Overzicht van alle REST API calls](./rest-api)
* [Opvragen van een Publisher destination](./rest-get-publisher-destination)
* [Opvragen van abuses voor een Publisher destination](./rest-get-publisher-destination-abuses)
* [Opvragen van deliveries voor een Publisher destination](./rest-get-publisher-destination-deliveries)
* [Opvragen van errors voor een Publisher destination](./rest-get-publisher-destination-errors)
* [Opvragen van impressions voor een Publisher destination](./rest-get-publisher-destination-impressions)
* [Opvragen van unsubscribes voor een Publisher destination](./rest-get-publisher-destination-unsubscribes)