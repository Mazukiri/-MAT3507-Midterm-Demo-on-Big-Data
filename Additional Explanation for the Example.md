Listing 9-1: Importing the FSIS Meat, Poultry, and Egg Inspection Directory
This script creates a table to store data from the FSIS inspection directory and loads the data from a CSV file into the table using the COPY command. It also creates an index on the company column for faster querying.

Listing 9-2: Finding multiple companies at the same address
This query identifies companies sharing the same address by grouping records by company, street, city, and st and counting duplicates.

Listing 9-3: Grouping and counting states
The query groups records by the st column to count how many establishments are listed per state.

Listing 9-4: Using IS NULL to find missing values in the st column
This query identifies records where the st (state) column is empty, which may indicate missing or incomplete data.

Listing 9-5: Using GROUP BY and count() to find inconsistent company names
This groups records by company and counts occurrences, helping identify potential inconsistencies in company names.

Listing 9-6: Using length() and count() to test the zip column
The query checks the length of zip codes and counts how many records fall into each length category, which helps identify formatting issues.

Listing 9-7: Filtering with length() to find short zip values
This filters records where zip codes are shorter than five characters, identifying incomplete postal codes.

Listing 9-8: Backing up a table
This creates a backup of the meat_poultry_egg_inspect table, storing an identical copy to safeguard data during experimentation.

Listing 9-9: Creating and filling the st_copy column
This adds a new st_copy column to store a copy of st values, creating a backup for future updates.

Listing 9-10: Checking values in the st and st_copy columns
This query displays the original and copied state (st) columns to verify the backup process.

Listing 9-11: Updating the st column for three establishments
This updates the st (state) column for three specific establishments based on their est_number.

Listing 9-12: Restoring original st column values
This restores the st column values from either the st_copy column or the backup table.

Listing 9-13: Creating and filling the company_standard column
This adds a company_standard column to store cleaned or standardized company names, initially duplicating the company column.

Listing 9-14: Use UPDATE to modify field values that match a string
This standardizes company names starting with "Armour" by updating company_standard to a consistent format.

Listing 9-15: Creating and filling the zip_copy column
This adds a zip_copy column and copies zip values into it for backup purposes.

Listings 9-16 and 9-17: Modifying zip codes missing leading zeros
These scripts fix incomplete zip codes by prepending missing zeros for specific states.

Listing 9-18: Creating and filling a state_regions table
This creates a table mapping states to regions and populates it with data from a CSV file.

Listing 9-19: Adding and updating an inspection_date column
This adds an inspection_date column and updates it for establishments in the "New England" region using the state_regions table.

Listing 9-20: Viewing updated inspection_date values
This query displays states and their corresponding inspection dates to verify updates.

Listing 9-21: Delete rows matching an expression
This deletes records for establishments located in Puerto Rico (PR) and the Virgin Islands (VI).

Listing 9-22: Remove a column from a table using DROP
This removes the zip_copy column from the table.

Listing 9-23: Remove a table from a database using DROP
This deletes the meat_poultry_egg_inspect_backup table permanently from the database.

Listing 9-24: Demonstrating a transaction block
This uses a transaction block to update a company name, preview the change, and either commit or rollback the update.

Listing 9-25: Backing up a table while adding and filling a new column
This creates a backup of the table and adds a new column (reviewed_date) to indicate when the backup was created.

Listing 9-26: Swapping table names using ALTER TABLE
This swaps the names of the main table and its backup, effectively restoring the backup as the active table.
