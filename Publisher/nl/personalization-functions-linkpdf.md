# Personalisatie functies: linkpdf

De linkpdf tag kan gebruikt worden om een link op te stellen naar een 
bestaand PDF bestand. Eerst moet er een document of template gevonden 
worden dat matcht met de aanvraag. Deze wordt dan omgezet naar een link, 
die automatisch escaped wordt, tenzij anders gespecificeerd.

## Voorbeeld

    {linkpdf document="mypreviousmailing" escape="true"}
    
Dit geeft alleen de link zelf weer, maar je kunt altijd HTML gebruiken 
om de link te vervangen door woorden en klikbaar te maken.

## Meer informatie

* [Personalisatie](./personalization)
* [Personalisatie functies](./personalization-functions)