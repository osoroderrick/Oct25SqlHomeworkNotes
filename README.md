# Oct25SqlHomeworkNotes
```
*SQL purpose:
  -To manipulate sets  of data 
  -Typically from a relational database
  -ANSI and ISO standards
*A database is a name given to container that helps organize data and a logical way that allows for efficient storage and retrieval of data
*Each column in a table has restrictions type, format, and size
*Query in the database is asking questions of the database and hopefully being provided with an answer
*Database design controls what questions you can ask later
*SQL Claus's consists of keywords and identifiers
*Select is a command that allows you to retrieve one or more rows from one or more tables
*Insert into command:
    -adds one or more rows into a single table
*Update:
    -modifies one or more rows in a table
*Delete from :
    -removes one or more rows from one table
*The select list:
 -Contains a list of columns from a table you want to query
  -From Clause is required
  -After every column comes a, except the last column

*From clause defines the table you want to query
*It is good practice to always table qualify the names of your columns
*Alias the table name for quicker typing
*The ways to constrain results are to use where clause or distinct clause

*Where:
    -contains Boolean expression
    -comes after from clause
    -constrains results set
    -only matching rows are in the result set

And:
 -Combines two expressions
-If both are true, row is included
-If those are false, Roe is excluded

Or:
 -Combines two expressions
-If either are true, row is included  
-If either are false row is excluded

Between:
  -Acts on column and two values
  -True if column value is between two values
  -Inclusive include two values like (>= & <=)

Like:
  -String with special characters inside
  -If match is true row is returned

In:
  -Like or operator
  -List of potential values
  -Like a multi value = operator
  -True if any of the values in the list hit

Is:
  -Special operator
  -Like in equals operator
  -But just for values that might be null

  Is not:
  -Also just for null
  -like a not equals operator

Order by:
  -Allow sorting of result set
  -After the where Clause (if there is one)
  -Specify one or more columns
  -Separate columns by columns
  -ASC (default)  for DESC 

Set functions:
  -Computes new values from  column values
  -Use in place of columns Inn Select clause
  -Passes column name to function
  -Helps us to ask more interesting questions
  -Often used with distinct qualifier
  
*Count- count of all the column specified (includes null values if *  used)

*Max- maximum value of the column (does not include null values)

*Min-  minimum value of the column (does not include null  values)

*AVG -  average of all the column (does not include null value, only numeric column)

*Sum -  sum of all the value of  the column (does not include null values only numeric column)

Set functions and qualifiers:
   -Often used together
  -Add inside function
  -Run against distinct column values
  
Group by:
  -Allows multiple columns with a set function
  -Breaks results set into subset  
  - Runs set function against each subset
  - Results set returns one row per subset
  - Subset is dictated by column in group by
  - Column must appear in the select list
  - Appears after from and/or where clauses
  
  *Having:
  - Works like where works against select
  - Restrict the subset

*Cross join:
  - Simplest join
  - All rows from both tables
  - No where clause
  - Least useful
  - Inefficient
  - Cartesian product
  - Cross Key Word implied

* Inner join:
  - Most typical join
  -Emphasizes relational nature of databases
  - Matches column in the first table to the second
  -Primary key to foreign key is most common

* Outer join:
  - Inner join doesn't deal with null values
  -Outer join works even with no match
  -Null columns null match is second table
  - Full outer join returns all joined rows
  - Know when no match is in either  table

* Left outer join:
  - Another  null  related join
  - All rows from the left side will be returned
  - Null for non-matching right side table

* Right outer join:
  - Opposite of left outer join
  - All rows from the right side will be returned
  - Null for non-matching left side table

* Full outer join
  - Merging of left and right outer join
  - Union distinct in MySQL

* Self join:
  - Join table on itself
  -No special syntax
  -Same table on left and right side of join
  -Useful when table contains hierarchical  data 
