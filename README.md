# Auto-Sequences-and-Triggers-Creator
SQL code that creates sequences and triggers for primary keys in a Oracle database.

# Technology
The SQL code was written for an Oracle database and should work on any version of Oracle that supports sequences and triggers.

## Functionality
get_table_primary_keys function
This function returns a cursor that contains the names of tables and their primary key columns. The function only returns tables that have a primary key column of data type NUMBER.

create_sequences_and_triggers procedure
This procedure drops all existing sequences and creates new ones for each primary key column in the tables returned by the get_table_primary_keys function. For each table, the procedure retrieves the current maximum value of the primary key column and creates a new sequence that starts from the next value. It then creates a trigger for the table that sets the value of the primary key column to the next value of the sequence before inserting a new row into the table.

How to Use
Open Oracle SQL Developer or any other SQL client that can connect to an Oracle database.
Connect to the Oracle database where you want to create the sequences and triggers.
Open a new SQL worksheet or file.
Copy the code from the create_sequences_and_triggers.sql file in this repository and paste it into the SQL worksheet or file.
Execute the code.
Note: Make sure to execute the code as a user that has privileges to create sequences and triggers.

Contribution
If you find any issues or want to add any new features, feel free to open a pull request or an issue.





