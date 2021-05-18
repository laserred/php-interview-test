# Project Brief

## The Problem
We've been provided a CSV from a supplier with some new products we'd like to start stocking. We need a way to import this data for the sales department to easily see.

The supplier will be sending this CSV weekly, so existing products will need updating if their stock, price, or other details change (their code will not).

## The Solution 
Using Laravel, create a way to import the new products (either console command or file upload), correctly parsing the contents of the CSV. When the import is processed, it will need to report how many items were processed, how many were successful, how many were skipped (see the import rules below).

Sales staff will also need a way to see this data, so a table showing the contents of the database is required.

The import must be able to run in 'test' mode to allow the importer to review what will happen - we don't want them selling the wrong products! This mode should act as a normal import, but not actually save the data.

## Import Rules 
1. Items that cost less than £5 and have a quantity less than 10 will not be imported.
2. Items that cost over £1000 will not be imported.
3. Discontinued items will be imported but need their discontinued date set at the time of import.

## Tips 
This CSV came from an external source, we will need extra validation to make sure it's formatted correcly and has no encoding issues.