🏠 Description of JHouse — Real Estate Data Manager in C
JHouse is a command-line (CLI) program written in C that allows you to display, search, sort, and export real estate property data from a CSV file. It’s designed for working with datasets containing location, price, rooms, bathrooms, and more.

📌 Features
1. Display Data — Show a set number of property listings from the CSV file.
2. Search Data — Find properties by:
- Location
- City
- Price
- Number of Rooms
- Number of Bathrooms
- Number of Carparks
- Type of property
- Furnishing status
3. Sort Data — Sort by any column in ascending (asc) or descending (desc) order.
4. Export Data — Save the currently displayed or searched data into a new .csv file.


📄 CSV Format
The program reads data from file.csv with the following semicolon-separated format:
Location; City; Price; Rooms; Bathroom; Carpark; Type; Furnish
123 Main St; New York; 300000; 3; 2; 1; Apartment; Fully Furnished
456 Oak Ave; Chicago; 250000; 4; 3; 2; House; Semi Furnished
etc...
⚠️ Make sure the file uses ; (semicolon) as separators, except for the last column which ends at newline. For testing, please use the Jhouse_Data.csv

⚙️ How to Compile & Run
1. Compile: gcc main.c -o jhouse
2. Run: ./jhouse

🖥️ Usage Flow
When you run the program, you’ll see a menu:
JHouse
What do you want to do?
1. Display Data
2. Search Data
3. Sort Data
4. Export Data
5. Exit
   
1. Display Data
- Shows the first N rows from the dataset.

2. Search Data
- Enter a column name (e.g., City) and a value (e.g., Chicago).
- Displays all matching entries.

3. Sort Data
- Choose a column and sort order (asc / desc).
- Displays the first 10 sorted results.

4. Export Data
- Saves the currently displayed or searched data into a new CSV file.
- Allow custom filename input. Example: entering "output" will create "output.csv".

🛠 Example Run (Data is just an Example)
Location; City; Price; Rooms; Bathroom; Carpark; Type; Furnish
123 Main St; New York; 300000; 3; 2; 1; Apartment; Fully Furnished
456 Oak Ave; Chicago; 250000; 4; 3; 2; House; Semi Furnished
789 Pine Rd; Boston; 200000; 2; 1; 0; Condo; Unfurnished

JHouse
What do you want to do?
1. Display Data
2. Search Data
3. Sort Data
4. Export Data
5. Exit
Your choice: 1
Number of rows: 3

Location                 City                Price     Rooms     Bathroom  Carpark   Type        Furnish
123 Main St              New York            300000    3         2         1         Apartment   Fully Furnished
456 Oak Ave              Chicago             250000    4         3         2         House       Semi Furnished
789 Pine Rd              Boston              200000    2         1         0         Condo       Unfurnished

✍️ Author
- Johannes Aaron Framon

📌 Notes & Limitations
- The program is designed specifically for the Jhouse_Data file, making up to 4000 rows of data.
- Data is loaded fresh from the CSV for each search/sort.
- Sorting uses a bubble sort algorithm — fine for small datasets but not optimized for huge files.
- CSV must match the exact column order in the code.
