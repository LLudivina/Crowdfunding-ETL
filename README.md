# Crowdfunding-ETL
# Overview of Project

In this module, we were introduced to a crowdfunding platform called Independent Funding.  Once the platform became more popular for funding independent projects, data needed to be stored in a database.  Hence, we were tasked with helping, Britta, a junior SQL developer, move the data to a database and generate reports for stakeholders.  This way, we also learn about the extract, transform, and load (ETL) process used to create a data pipeline.  However, towards the end of the ETL process, new data was received and had to be analyzed.  

## Purpose
The purpose of this project was to carry out the ETL process and data analysis on the new dataset from the backers info that have pledged to the live projects. 

# Results
The extract and transform phases were done using Python, Pandas, and Jupyter notebook.  Once the data was collected and cleaned, an entity relationship diagram (ERD) and table schema were created as a guide for storing the data in a database that was created using PostgressSQL.  

When updating the ERD and table schema, the primary and foreign keys from the backers csv file had to be carefully checked to confirm that they referenced the relevant table.  As seen in Figure 1, the Backers foreign key (cf_id) references the Campaign table's primary key (cf_id).

## *Figure 1*
![Alt text](resources/crowdfunding_db_relationships.png)

As a visual piece of information, the ERD came in handy when loading the data into the tables in pgAdmin 4. This is because as mentioned in the module tables referenced by a foreign key constraint on another table, must be imported first or we get an error message.  There are other things to consider as well. For example, it took me a while to figure out how to import the data for the campaign table because there was an extra column that went unnoticed.  Once I went back and corrected the mistake, data importing was a success.  Once all the data was imported into the corresponding tables, an SQL Analysis was conducted to create a final table with information about the remaining goal amounts.

# Summary
Overall, ETL is a very long process that requires a lot of attention to detail.  It is crucial to clearly understand the end goal and process needed to reach such end goal.  Otherwise, you can easily find yourself retracing your steps to fix the problem.  This can be very time consuming when dealing with massive amounts of data. 




