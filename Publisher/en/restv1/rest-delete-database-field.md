# REST API: DELETE database field

Warning: You are viewing the documentation for the old REST API. We recommend 
using [version 2](../restv2/rest-api.md) of the REST API.

When you send an HTTP DELETE request to the following URL, you’ll delete 
a field from a database:

`https://api.copernica.com/v1/database/$id/field/$id?access_token=xxxx`

The $id needs to be replaced by the numerical identifier, the ID, of the 
database. The second needs to be replaced by the ID or the name of the 
field you want to delete.

## PHP example

The following example demonstrates how to make a call using this method.

```php
// dependencies
require_once('copernica_rest_api.php');

// change this into your access token
$api = new CopernicaRestApi("your-access-token");

// do the call
$api->delete("database/1234/field/firstname");
```

The example above requires the [CopernicaRestApi class](rest-php).

## More information
- [Overview of all API calls](rest-api)
- [GET database fields](rest-get-database-fields)
- [POST database field](rest-post-database-fields)
- [PUT database field](rest-put-database-field)
