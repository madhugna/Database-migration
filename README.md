# Database-migration

COMPANY: CODETECH IT SOLUTIONS

NAME: MADHUGNA KADEM

INTERN ID: CT04DN607

DOMAIN: SQL

DURATION: 4 WEEKS

MENTOR: NEELA SANTHOSH KUMAR

-> Task Overview

This task was all about migrating data from a MySQL database to a PostgreSQL database. Instead of using any third-party tools like pgLoader or DBeaver, we followed a simple manual method to complete this migration. The goal was to move both the database structure and the data from MySQL to PostgreSQL without losing anything and ensuring everything worked correctly in the new environment.

We started by exporting the data from the MySQL database using a command-line tool. This process created a SQL dump file that contains all the commands needed to recreate the database tables and insert the data. The command we used was mysqldump, which is commonly used to back up MySQL databases. We saved the output into a file, which we later used for the import step.

Once the SQL file was ready, we opened it in a text editor and made a few changes to make it compatible with PostgreSQL. This step is important because MySQL and PostgreSQL use slightly different SQL syntax. For example, MySQL uses AUTO_INCREMENT for automatically increasing numbers, while PostgreSQL uses SERIAL or GENERATED columns. We also removed or replaced MySQL-specific features like backticks (), ENGINE=InnoDB, and adjusted data types such as changing TINYINTtoSMALLINTandDATETIMEtoTIMESTAMP`. After making these changes, the SQL file was ready to be used in PostgreSQL.

Next, we opened PostgreSQL and created a new database where we would import the data. We used a simple SQL command like CREATE DATABASE new_db_name; to do this. Then, we used the psql command-line tool to import the modified SQL file into the new PostgreSQL database. The import command reads all the SQL statements from the file and runs them inside the new database, creating tables and inserting data just like it was in MySQL.

After the import was completed, we tested everything to make sure the migration was successful. We ran a few SQL queries like SELECT * FROM table_name; and SELECT COUNT(*) to check that the data had been correctly copied. We verified that the number of rows in each table matched the original MySQL database and that all table structures were created properly.

Overall, this manual method helped us understand the differences between MySQL and PostgreSQL, and gave us full control over the migration process. It’s a great approach when you want to learn how things work under the hood or when you can't use external tools. At the end of this task, we had a fully working PostgreSQL database with all the original data from MySQL safely migrated.

This task also helped us improve our SQL skills, get comfortable with database commands, and understand how to handle compatibility issues between different database systems. The deliverables for this task include the original SQL dump file, the edited version for PostgreSQL, a step-by-step migration report, and screenshots or output of SQL queries that confirm the migration was successful.
