# Database Management System
## Introduction:
  * ## Database: 
      Database is a collection of inter-related data which helps in efficient retrieval, insertion and deletion of data from database and organizes the data in the form of tables, views, schemas, reports etc.
  * ## Database Management System:
       It s a software for storing and retrieving users' data while considering appropriate security measures. It consists of a group of programs which manipulate the database. The DBMS accepts the request for data from an application and instructs the operating system to provide the specific data. In large systems, a DBMS helps users and other third-party software to store and retrieve data.
   * ## Other Important Terminologies:
        * <b>Data Definition:</b> It helps in creation, modification and removal of definitions that define the organization of data in database.
        * <b>Data Updation:</b> It helps in insertion, modification and deletion of the actual data in the database.
        * <b>Data Retrieval:</b> It helps in retrieval of data from the database which can be used by applications for various purposes.
        * <b>User Administration:</b> It helps in registering and monitoring users, enforcing data security, monitoring performance, maintaining data integrity, dealing with concurrency control and recovering information corrupted by unexpected failure.
        * [DDL](#DDL)
        * [DML](#DML)
        * [DCL](#DCL)
        * [TCL](#TCL)
     
## SQL:
## DDL:
DDL is short name of Data Definition Language, which deals with database schemas and
descriptions, of how the data should reside in the database.<br>
● CREATE - to create a database and its objects like (table, index, views, store procedure,
function, and triggers)<br>
● ALTER - alters the structure of the existing database<br>
● DROP - delete objects from the database<br>
● TRUNCATE - remove all records from a table, including all spaces allocated for the
records are removed<br>
● RENAME - rename an object<br>

## DML:
DML is short name of Data Manipulation Language which deals with data manipulation and
includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is
used to store, modify, retrieve, delete and update data in a database.<br>
● SELECT - retrieve data from a database<br>
● INSERT - insert data into a table<br>
● UPDATE - updates existing data within a table<br>
● DELETE - Delete all records from a database table<br>
● MERGE - UPSERT operation (insert or update)<br>

## DCL:
DCL is short name of Data Control Language which includes commands such as GRANT and
mostly concerned with rights, permissions and other controls of the database system.<br>
● GRANT - allow users access privileges to the database<br>
● REVOKE - withdraw users access privileges given by using the GRANT command

## TCL:
TCL is short name of Transaction Control Language which deals with a transaction within a database.<br>
● COMMIT - commits a Transaction<br>
● ROLLBACK - rollback a transaction in case of any error occurs<br>
● SAVEPOINT - to roll back the transaction making points within groups
