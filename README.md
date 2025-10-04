This project aims to provide multilingual translation of generic and branded nutrition data compiled from various available public sources in an easily digestible format for applications.

# Sources

## Generic Sources
  - [Swiss Food Composition Database](https://naehrwertdaten.ch/en/)

## Branded Sources

# Naming conventions
## Files
- Generic: generic_\[source_name\]_\[product_or_recipe\],
- Branded: branded_\[brand_name\]_product

## Fields
- *ID*: unique ID number within the repository, assigned in ascending order of addition to the repository.
- *date_updated*: date of product data being retrieved from the source URL, in yyyy-MM-dd format.
- *source*: URL of the publicly available source from where the data was retrieved from. 
  - Archived on Wayback Machine at the time of retrieval.
- *ID_source*: unique identifier provided at the source URL for product differentiation.
- *date_updated_source*: date of product data being updated on the source URL (if available), in yyyy-MM-dd format.
  - Defaults to *date_updated* value if not available.
- *name_primary_\[lang\]*: standardized, colloquially accepted name of the product.
  - *lang* is 2-letter language code according to ISO-639-1 standard.
  - TODO: standardize primary naming convention for available products.
- *name_secondary_\[lang\]*: synonym names of the product.
  - *lang* is 2-letter language code according to ISO-639-1 standard.
- *categories_\[lang\]*: category taxonomy of the product.
  - *lang* is 2-letter language code according to ISO-639-1 standard.
  - TODO: standardize available category taxonomy to English, separate localization in other languages for category mapping in a separate file.
- *weight_package_g*: Package weight in grams. 
  - Provided only for branded products, and only if package size is different from serving size.
- *weight_serving_g*: Serving weight in grams (if available).
  - Provided only if available in the original source.

The rest of the fields contain actual nutrition data as provided in the data source, naming standardized and values normalized to "grams per 100 grams of product" measurements.