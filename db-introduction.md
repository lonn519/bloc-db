> What data types do each of these values represent?

- "A Clockwork Orange" - String
- 42 - Integer
- 09/02/1945 - DateTime
- 98.7 - Float
- $15.99 - Currency

> Explain when a database would be used. Explain when a text file would be used.

You would use a database if you needed:
- to store data even when the application is not running
- have multiple people accessing it 
- add, retrieve, delete, modify data often

You would use a textfile.
- simple appending of data, like log files
- retrieval not too important
- want to write the data fast

> Describe one difference between SQL and other programming languages.
- the = sign is used for 'equality'.

> In your own words, explain how the pieces of a database system fit together at a high level.
- A database consists of tables, which contain records on one topic. Columns provide the headers for those records.

> Explain the meaning of table, row, column, and value.
- A table contains rows and columns of values. Columns are the headers of the table and describe the type of data. Rows correspond to individual records. Value is what is stored in each cell.

> List three data types that can be used in a table.
- Integer
- String
- Float

> Given this payments table, provide an English description of the following queries and include their results:

Description: Show all the dates and amounts from the payments table.
**Query #1**

    SELECT date, amount FROM payments;

| date                     | amount    |
| ------------------------ | --------- |
| 2016-05-01T00:00:00.000Z | 1500.0000 |
| 2016-05-10T00:00:00.000Z | 37.0000   |
| 2016-05-15T00:00:00.000Z | 124.9300  |
| 2016-05-23T00:00:00.000Z | 54.7200   |
---


Description: Show all the amounts that are greater than 500 in the payments table.
**Query #2**

    SELECT amount FROM payments WHERE amount > 500;

| amount    |
| --------- |
| 1500.0000 |

---
Description: Show the date, payee, amount and memo where the payee is Mega Foods.
**Query #3**

    SELECT *FROM payments WHERE payee = 'Mega Foods';

| date                     | payee      | amount   | memo      |
| ------------------------ | ---------- | -------- | --------- |
| 2016-05-15T00:00:00.000Z | Mega Foods | 124.9300 | Groceries |

---


Given this users table, write SQL queries using the following criteria and include the output:

The email and sign-up date for the user named DeAndre Data.
Select email, signup from users where name='DeAndre Data';

The user ID for the user with email 'aleesia.algorithm@uw.edu'.
Select userid where email='aleesia.algorithm@uw.edu';

All the columns for the user ID equal to 4.
Select * where userid=4;

**Query #1**

    Select email, signup from users where name='DeAndre Data';

| email             | signup                   |
| ----------------- | ------------------------ |
| datad@comcast.net | 2008-01-20T00:00:00.000Z |

---
**Query #2**

    Select userid from users where email='aleesia.algorithm@uw.edu';

| userid |
| ------ |
| 1      |

---
**Query #3**

    Select * from users where userid=4;

| userid | name           | email             | signup                   |
| ------ | -------------- | ----------------- | ------------------------ |
| 4      | Brandy Boolean | bboolean@nasa.gov | 1999-10-15T00:00:00.000Z |

---
