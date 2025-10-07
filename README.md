This project aims to provide multilingual translation of generic and branded nutrition data compiled from various available public sources in an easily digestible format for applications.

# Sources

|Type|Source|Product or recipe|Available languages|Notes|
|---|---|---|---|---|
|Generic|[Swiss Food Composition Database](https://naehrwertdaten.ch/en/)|Product|en,de,fr,it,uk|Focuses on generic food ingredients, dishes available in the EU. Sometimes uses unconventional English translations due to Swiss origin.|
|Branded|[MenuStat](https://www.menustat.org)|Product|en|Focuses on dishes available in American fast food chains. While data has not been updated since 2022, it remains reasonably accurate for purposes of nutrition estimates.|
|Generic|[Nederlands Voedingsstoffenbestand (NEVO)](https://www.rivm.nl)|Product|en,nl|Focuses on generic food ingredients, dishes available in the EU.|

# Fields
|Name|Description|Notes|TODO|
|---|---|---|
|*ID*|Unique identifier of the food product/recipe data within the repository.|Assigned in ascending order at the time of addition to the repository.||
|*date_updated*|Date of product data being retrieved from the source URL.|Provided in yyyy-MM-dd format.||
|*source*|URL of the publicly available source from where the data was retrieved from.|Archived on Wayback Machine at the time of retrieval.||
|*ID_source*|Unique identifier of the food product/recipe data provided at the source URL for product differentiation.|N/A||
|*date_updated_source*|Date of product data being updated on the source URL (if available).|Provided in yyyy-MM-dd format, defaults to *date_updated* value if not available.||
|*name_primary_\[lang\]*|Standardized, colloquially accepted name of the product.|*lang* is 2-letter language code according to ISO-639-1 standard.|TODO: Standardize primary naming convention for available products.|
|*name_secondary_\[lang\]*|Synonym names of the product.|*lang* is 2-letter language code according to ISO-639-1 standard.|N/A|
|*categories_\[lang\]*|Category taxonomy of the product.|*lang* is 2-letter language code according to ISO-639-1 standard.|TODO: standardize available category taxonomy to English, separate localization in other languages for category mapping in a separate file.|
|*weight_package_g*|Package weight in grams.|Provided only for branded products, and only if package size is different from serving size.|N/A|
|*weight_serving_g*|Serving weight in grams (if available)|Provided only if available in the original source.|N/A|

The rest of the fields contain actual nutrition data as provided in the data source, naming standardized and values normalized to "grams per 100 grams of product" measurements.
