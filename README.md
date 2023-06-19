
# Assignment for Data Scientist
This project consists of two tasks, Assignment 1 and Assignment 2, both of which have been successfully completed. The project involves working with an Excel file and performing some data manipulation and analysis tasks using Excel and then usning Python to convert the Excel sheet into a csv file then using KMeans clustering to perform clustering on the dataset based on the feature called Division.

## Assignment 1: Excel

I have followed these steps to create the desired pivot table in Excel:

1. Open the Excel sheet containing the data (Sheet1).
2. Go to the "Insert" tab in the Excel ribbon and click on "PivotTable" under the Tables section.
3. In the "Create PivotTable" dialog box, ensure that "Select a table or range" is selected and that the correct range is displayed in the "Table/Range" field.
4. Choose where you want to place the pivot table. You can either select an existing worksheet or create a new one.
5. Click "OK" to create the pivot table.
6. In the PivotTable Field List, drag the "Division" field to the "Rows" area.
7. Drag the "Customer" field to the "Rows" area below the "Division" field.
8. Drag the "ID" field to the "Rows" area below the "Customer" field.
9. Drag the "Gender" field to the "Columns" area.
10. Drag the "Marital Status" field to the "Columns" area below the "Gender" field.
11. Drag the "Income" field to the "Values" area.
12. In the "Values" area, click on the drop-down arrow next to "Sum of Income" and select "Value Field Settings."
13. In the "Value Field Settings" dialog box, make sure that "Sum" is selected and click "OK."

This is how i have created the pivot table, which displays the sum of income according to the specified structure. The sheet that contains the pivot table I named it as "PivotTable".

14. Then, to add a new column in sheet1, namely “Matched” which matches the IDs of sheet2 with the IDs of sheet1 and show the result as True or False, I've used this formula:

```bash
  =IF(ISNUMBER(MATCH(A2,Sheet2!A:A,0)),TRUE,FALSE)
```

## Additional Sheet:
Additionally I've added another sheet namely "Filter", using this sheet you can filter the values of sheet 1 with respect to 'Division', 'Gender', and 'Marital Status'.

## Assignment Part 2: Python
### Requirements:
- Pandas
- Seaborn
- Matplotlib
- Scikit-Learn
- Used Python Version: 3.10.3

If you don't have this libraries installed on your system. You can run this command to install these libraries:

```bash
    pip install -r requirements.txt
```
For the assignment 2 section I've approached this way:

1. To separate the sheet 1 data in a new excel sheet I've used pandas "read_excel" function.
2. Then to convert the excel file to csv, I've used "to_csv" function of pandas
3. Then to load the csv file I've used "read_csv" function.
4. Then to get rid of the column ID from the data frame, I've dropped the column using the "drop" function provided by pandas.
5. Then to have all the values of each categorical features except "Customer Name" into numerical format, I've used "LabelEncoder" function provided by Scikit-Learn.
6. Then to cluster the data based on Division I've used KMeans clustering algorithm provided by keras.

## Additional Work:
I've done a small data analysis and visualization on this dataset like:
- What is the proportion of data based on Gender?
- What is the Marital Status of different regions?
- Which division has the highest overall income?





    
