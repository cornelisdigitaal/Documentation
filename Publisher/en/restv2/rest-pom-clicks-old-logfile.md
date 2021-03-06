# Click Record (old style) Information

Every click on a link from messages sent via Publisher is logged in the "pom-clicks-old" log files. The data in a record depends on which tracking system is used, the article [new link tracking system](https://www.copernica.com/en/blog/post/new-link-tracking-system "New link tracking system") states more information about the different tracking systems. You can download the content of these files in CSV, JSON, and XML format using the [REST logfiles API](rest-get-logfiles), or the dashboard. These log files contain the following data in the respective order:

| Data         | Description                                             |
| ------------ | ------------------------------------------------------- |
| id           | The ID of the message from which was clicked            |
| time         | The time when the click occurred                        |
| ip           | The IP address that clicked                             |
| header       | The header of the request form the click                |
| email        | The email address to which the mail was originally sent |
| tags         | The tags of the message (semicolon separated)           |
| countrycode  | The code of the country in which the click occurred     |
| countryname  | The name of the country in which the click occurred     |
| regioncode   | The code of the region in which the click occurred      |
| city         | The name of the city in which the click occurred        |
| senderdomain | The sender domain from which the message was sent       |
| groupid      | The ID of the group to which the mail belonged to       |
| profile      | The ID of the profile                                   |
| subprofile   | The ID of the subprofile                                |
| template     | The ID of the used template                             |
| document     | The ID of the used document                             |

## Other logfile names

* [Marketing Suite general log](./rest-cdm-attempts-logfile)
* [Marketing Suite abuse log](./rest-cdm-abuse-logfile)
* [Marketing Suite click log](./rest-cdm-click-logfile)
* [Marketing Suite delivery log](./rest-cdm-delivery-logfile)
* [Marketing Suite error log](./rest-cdm-error-logfile)
* [Marketing Suite impressions log](./rest-cdm-impression-logfile)
* [Marketing Suite retry log](./rest-cdm-retry-logfile)
* [Marketing Suite unsubscribe log](./rest-cdm-impression-logfile)
* [Publisher general log](./rest-pom-attempts-logfile)
* [Publisher abuse log](./rest-pom-abuses-logfile)
* [Publisher clicks (new style) log](./rest-pom-clicks-logfile)
* [Publisher delivery log](./rest-pom-deliveries-logfile)
* [Publisher error log](./rest-pom-errors-logfile)
* [Publisher impressions log](./rest-pom-impressions-logfile)
* [Publisher retry log](./rest-pom-retries-logfile)
* [Publisher unsubscribe log](./rest-pom-unsubscribes-logfile)

## More information on logfiles

* [List of all API calls](rest-api)
* [GET logfiles names](rest-get-logfiles-names)
* [GET logfiles JSON](./rest-get-logfiles-json.md)
* [GET logfiles CSV](./rest-get-logfiles-csv.md)
* [GET logfiles XML](./rest-get-logfiles-xml.md)
