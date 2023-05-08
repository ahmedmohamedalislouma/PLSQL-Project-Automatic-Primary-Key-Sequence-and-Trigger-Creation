# PLSQL-Project-Automatic-Primary-Key-Sequence-and-Trigger-Creation
## Project Description

This PL/SQL script is designed to create a new sequence and trigger for each primary key column in a database schema. The sequence starts at the maximum value of the primary key column plus one and increments by one for each new row inserted into the table. The trigger is set to execute before each insert and assigns the next value from the sequence to the primary key column of the new row.

## Project Details

This PL/SQL script uses two cursors to loop through all of the primary key columns in a database schema. The first cursor selects all of the sequences in the schema, and the second cursor selects all of the primary key columns. For each primary key column, the script creates a new sequence with a name of "{table_name}_SEQ", where {table_name} is the name of the table containing the primary key column. The sequence starts with a value of the maximum primary key value in the table plus one and increments by one for each new row inserted into the table. The script also creates a trigger with a name of "{table_name}_TRG" that executes before each insert into the table. The trigger assigns the next value from the sequence to the primary key column of the new row.

## How to Use

To use this script, copy and paste it into a new SQL script in an SQL editor, such as SQL Developer or TOAD. Then, execute the script in the database schema where you want to create the sequences and triggers. Once the script has executed successfully, all of the primary key columns in the schema will have a new sequence and trigger created for them.

## Tools and Technologies

This script was written using PL/SQL and is compatible with any database that supports PL/SQL. It was tested using Oracle Database 19c and SQL Developer.
