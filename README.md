# Creating a Calendar Table Using the Power Query M-Language
# INTRODUCTION
Calendar Date table can be created in Power BI using mostly DAX. However, there might be reasons one might want to do the same using Power Query M language which might be for Model Performance reasons or convenience reasons. In this i have created the calendar date table using a Insert Column and the M language in Power Query. 
# STEPS FOR CREATING THE CALENDAR TABLE 
1. Create a new table named "**Calendar table**" from the home tab using the enter data table. ,change the column name and the table name to " **start date**" and enter the start date you wish to enter and load the data .
2. select the start date query and from the add column ribbon choose custom column option and create a column named "**End date**", then in the custom column formula type - **Date.From(DateTime.LocalNow())** and enter ok . 
3. Change the datatype of both the columns to date type.
4. Again from the add column ribbon choose custom column name as **"Dates"** and enter the formula as **{Number.From([#"start date "])..Number.From([#"End date "])}** click ok , expand the Dates column to new rows , change the datatype . Delete the **start date**" and "**End date** columns . 
5. Load Calendar dates table to Power BI data model and add start of year , month, day, week, quarter etc from the Date options . 
6.Open the "Advanced Editor" window to see the full M code behind this Calendar table .

