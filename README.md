In this demo, we will use PostgreSQL to clean up dirty data as well as perform other useful maintainance tasks.

For this example, we'll use a directory of U.S. meat, poultry, and egg produc ers. The Food Safety and Inspection Service (FSIS), an agency within the month. The FSIS is responsible for inspecting animals and food at more than U.S. Department of Agriculture, compiles and updates this database tors find a problem, such as bacterial contamination or mislabeled food, the 6,000 meat processing plants, slaughterhouses, farms, and the like. If inspec agency can issue a recall. Anyone interested in agriculture business, food s ply chain, or outbreaks of foodborne illnesses will find the directory useful. Read more about the agency on its site at https://www.fsis.usda.gov/. The file we'll use comes from the directory's page on https://www.data.gov/, a website run by the U.S. federal government that catalogs thousands of data sets from various federal agencies (https://catalog.data.gov/dataset/meat-poultry-and-egg-inspection-directory-by-establishment-name/). We'll examine the original data as it was available for download, with the exception of the ZIP Codes column.

To import the file into PostgreSQL, use the code in Listing 9-1 to create a table called meat_poultry_egg_inspect and use COPY to add the CSV file to the table. Use pgAdmin to connect to your database, and then open the Query Tool to run the code. Remember to change the path in the COPY statement to reflect the location of your CSV file.

This demo highlights our team's diverse skill set in Big Data, including data cleaning, executing complex queries on large databases, and employing techniques to gain deeper insights into the entire dataset.
