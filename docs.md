## Records without keyphrases

* Retrieves a list of skus from the website that don't exist in the `'autocomplete_order'` table.
* Retrieves the corresponding titles from Vova's list.
* If the 'Hide SKUs' checkbox is selected, any skus that exist in the `'hidden_skus.txt'` file are removed from the list.
* The 2 columns of data (sku, title), plus an empty `'keyphrase'` column, are output to a TSV (Tab Separated Values) file.

Note: SKUs are enclosed in single quotes to avoid any leading zeros being omitted.

## All records with keyphrases

* Retrieve list of skus (keys) and keyphrases (values) from the `'autocomplete_order'` table.
* Retrieve list of skus (keys) and titles (values) from the `'sku_titles'` table (`'lookup_variations_titles'` database).
* Create a TSV (Tab Separated Values) file with 3 columns of data (keyphrase, sku, title).

Notes:
* SKUs are enclosed in single quotes to avoid any leading zeros being omitted.
* If any skus that exist in `'autocomplete_order'` are missing from `'sku_titles'` then `'NONE'`  is substituted for the title.

## All records without prices

* Retrieves a list of skus and prices from the website.
* Retrieve list of skus (keys) and keyphrases (values) from the `'autocomplete_order'` table.
* Retrieve list of skus (keys) and titles (values) from the `'sku_titles'` table (`'lookup_variations_titles'` database).
* Create a TSV (Tab Separated Values) file with 3 columns of data (keyphrase, sku, title). Records with skus that don't have a corresponding price on the website are omitted.

Notes:
* SKUs are enclosed in single quotes to avoid any leading zeros being omitted.
* If any skus that exist in `'autocomplete_order'` are missing from `'sku_titles'` then `'NONE'`  is substituted for the title.

## Skus that only exist on website

NOTES_HERE
