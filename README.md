# Database Management System
## Introduction:
  * ## Database: 
      Database is a collection of inter-related data which helps in efficient retrieval, insertion and deletion of data from database and organizes the data in the form of tables, views, schemas, reports etc.
  * ## Database Management System:
       It s a software for storing and retrieving users' data while considering appropriate security measures. It consists of a group of programs which manipulate the database. The DBMS accepts the request for data from an application and instructs the operating system to provide the specific data. In large systems, a DBMS helps users and other third-party software to store and retrieve data.<br>
       <br>
       <i> Database management systems were developed to handle the following difficulties of typical File-processing systems supported by conventional operating systems.<br>
       1) Redundancy of data
       2) Inconsistency of Data
       3) Difficult Data Access
       4) Unauthorized Access
       5) No Concurrent Access
       6) Atomicity of updates
       7) Backup and Recovery </i>
   * ## Other Important Terminologies:
        * <b>Data Definition:</b> It helps in creation, modification and removal of definitions that define the organization of data in database.
        * <b>Data Updation:</b> It helps in insertion, modification and deletion of the actual data in the database.
        * <b>Data Retrieval:</b> It helps in retrieval of data from the database which can be used by applications for various purposes.
        * <b>User Administration:</b> It helps in registering and monitoring users, enforcing data security, monitoring performance, maintaining data integrity, dealing with concurrency control and recovering information corrupted by unexpected failure.
        * [DDL](#DDL)
        * [DML](#DML)
        * [DCL](#DCL)
        * [TCL](#TCL)
      
## Architecture:
<b>3-Tier Architecture in DBMS: </b>DBMS 3-tier architecture divides the complete system into three inter-related but independent modules as shown below:
![image](https://user-images.githubusercontent.com/79071810/147411962-e3a63e61-0907-4802-8e68-626ea37165fc.png)<br>

* Physical Level: <i>At the physical level, the information about the location of database objects in the data store is kept. Various users of DBMS are unaware of the locations of these objects.In simple terms,physical level of a database describes how the data is being stored in secondary storage devices like disks and tapes and also gives insights on additional storage details.</i>
* Conceptual Level: <i>At conceptual level, data is represented in the form of various database tables. For Example, STUDENT database may contain STUDENT and COURSE tables which will be visible to users but users are unaware of their storage.Also referred as logical schema,it describes what kind of data is to be stored in the database.</i>
* External Level:  <i>An external level specifies a view of the data in terms of conceptual level tables.  Each external level view is used to cater to the needs of a particular category of users. For Example, FACULTY of a university is interested in looking course details of students, STUDENTS are interested in looking at all details related to academics, accounts, courses and hostel details as well. So, different views can be generated for different users. The main focus of external level is data abstraction.</i>

* <b>Data Independence: </b><i>Data independence means a change of data at one level should not affect another level. Two types of data independence are present in this architecture:</i><br>
  * Physical Data Independence: <i>Any change in the physical location of tables and indexes should not affect the conceptual level or external view of data. This data independence is easy to achieve and implemented by most of the DBMS.</i>
  * Conceptual Data Independence: <i>The data at conceptual level schema and external level schema must be independent. This means a change in conceptual schema should not affect external schema. e.g.; Adding or deleting attributes of a table should not affect the user’s view of the table. But this type of independence is difficult to achieve as compared to physical data independence because the changes in conceptual schema are reflected in the user’s view.<i>

     
## SQL:
* ## DDL:
     DDL is short name of Data Definition Language, which deals with database schemas and
descriptions, of how the data should reside in the database.<br>
● CREATE - to create a database and its objects like (table, index, views, store procedure,
function, and triggers)<br>
● ALTER - alters the structure of the existing database<br>
● DROP - delete objects from the database<br>
● TRUNCATE - remove all records from a table, including all spaces allocated for the
records are removed<br>
● RENAME - rename an object<br>

* ## DML:
     DML is short name of Data Manipulation Language which deals with data manipulation and
includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE, etc., and it is
used to store, modify, retrieve, delete and update data in a database.<br>
● SELECT - retrieve data from a database<br>
● INSERT - insert data into a table<br>
● UPDATE - updates existing data within a table<br>
● DELETE - Delete all records from a database table<br>
● MERGE - UPSERT operation (insert or update)<br>

* ## DCL:
     DCL is short name of Data Control Language which includes commands such as GRANT and
mostly concerned with rights, permissions and other controls of the database system.<br>
● GRANT - allow users access privileges to the database<br>
● REVOKE - withdraw users access privileges given by using the GRANT command

* ## TCL:
     TCL is short name of Transaction Control Language which deals with a transaction within a database.<br>
● COMMIT - commits a Transaction<br>
● ROLLBACK - rollback a transaction in case of any error occurs<br>
● SAVEPOINT - to roll back the transaction making points within groups
