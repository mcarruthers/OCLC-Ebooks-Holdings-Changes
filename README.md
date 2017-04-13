# OCLC-Ebooks-Holdings-Changes
**Process and scripts under development and subject to change.

1. Split files alphabetically 5 ways: 0-Dm, Dn-Dz, E-K, L-Nd, Ne-Z.
2. Combine each of five files with corresponding file from previous load.
3. Add additional columns (same as serials).
4. Save files as UTF-8 CSV.
5. Load each file into OpenRefine.<br/>
  a. Uncheck "Parse cell text into...", "Store blank rows"<br/>
  b. Set character encoding to UTF-8
6. Remove OSTI and ebrary titles by faceting on URL column.
7. Create new column by combining values from Title, Resource, and URL columns. Name new column "Combined".
8. Run duplicate facet on Combined.

For Add/Change:
1. Remove "true" from duplicate facet. (delete all matching rows)
2. Facet by Sheet Date. Delete "Earlier"
3. Remove Row Number, Sheet Date, and Combined.
4. Export spreadsheet as CSV.

For Delete:
1. Remove "true" from duplicate facet. (delete all matching rows)
2. Facet by Sheet Date. Delete "Later"
3. Remove Row Number, Sheet Date, and Combined.
4. Export spreadsheet as CSV.

After running all five spreadsheets through OpenRefine, combine results into a single spreadsheet for all Add/Change and all Delete.
