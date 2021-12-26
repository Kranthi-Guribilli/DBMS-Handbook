# Database Management System
## Introduction:
  * ## Database: 
      Database is a collection of inter-related data which helps in efficient retrieval, insertion and deletion of data from database and organizes the data in the form of tables, views, schemas, reports etc.
  * ## Database Management System:
       It s a software for storing and retrieving users' data while considering appropriate security measures. It consists of a group of programs which manipulate the database. The DBMS accepts the request for data from an application and instructs the operating system to provide the specific data. In large systems, a DBMS helps users and other third-party software to store and retrieve data.<br>
       <br>
       <i> Database management systems were developed to handle the following difficulties of typical File-processing systems supported by conventional operating systems.</i>
       * [Redundancy of data](#Data redundancy and inconsistency)
       *  Inconsistency of Data
       * Difficult Data Access
       * [Unauthorized Access](#Data security)
       * [No Concurrent Access](#Data concurrency)
       * Atomicity of updates
       * Backup and Recovery
   * ## Other Important Terminologies:
        * <b>Data Definition:</b> It helps in creation, modification and removal of definitions that define the organization of data in database.
        * <b>Data Updation:</b> It helps in insertion, modification and deletion of the actual data in the database.
        * <b>Data Retrieval:</b> It helps in retrieval of data from the database which can be used by applications for various purposes.
        * <b>User Administration:</b> It helps in registering and monitoring users, enforcing data security, monitoring performance, maintaining data integrity, dealing with concurrency control and recovering information corrupted by unexpected failure.
        * [DDL](#DDL)
        * [DML](#DML)
        * [DCL](#DCL)
        * [TCL](#TCL)
## Advantages of DBMS:
   * ## Data redundancy and inconsistency:
        Redundancy is the concept of repetition of data i.e. each data may have more than a single copy. The file system cannot control redundancy of data as each user defines and maintains the needed files for a specific application to run. There may be a possibility that two users are maintaining same files data for different applications. Hence changes made by one user does not reflect in files used by second users, which leads to inconsistency of data. Whereas DBMS controls redundancy by maintaining a single repository of data that is defined once and is accessed by many users. As there is no or less redundancy, data remains consistent.
   * ## Data sharing:
        File system does not allow sharing of data or sharing is too complex. Whereas in DBMS, data can be shared easily due to centralized system.
   * ## Data concurrency: 
        Concurrent access to data means more than one user is accessing the same data at the same time. Anomalies occur when changes made by one user gets lost because of changes made by other user. File system does not provide any procedure to stop anomalies. Whereas DBMS provides a locking system to stop anomalies to occur.
   * ## Data searching:
        For every search operation performed on file system, a different application program has to be written. While DBMS provides inbuilt searching operations. User only have to write a small query to retrieve data from database.
   * ## Data integrity:
        There may be cases when some constraints need to be applied on the data before inserting it in database. The file system does not provide any procedure to check these constraints automatically. Whereas DBMS maintains data integrity by enforcing user defined constraints on data by itself.
   * ## System crashing:
        In some cases,systems might have crashes due to various reasons. It is a bane in case of file systems because once the system crashes, there will be no recovery of the data that’s been lost. A DBMS will have the recovery manager which retrieves the data making it another advantage over file systems. 
  * ## Data security:
       A file system provides a password mechanism to protect the database but how longer can the password be protected?No one can guarantee that. This doesn’t happen in the case of DBMS. DBMS has specialized features that help provide shielding to its data.
## Architecture:
<b>3-Tier Architecture in DBMS: </b>DBMS 3-tier architecture divides the complete system into three inter-related but independent modules as shown below:
![image](https://user-images.githubusercontent.com/79071810/147411962-e3a63e61-0907-4802-8e68-626ea37165fc.png)<br>

* Physical Level: <i>At the physical level, the information about the location of database objects in the data store is kept. Various users of DBMS are unaware of the locations of these objects.In simple terms,physical level of a database describes how the data is being stored in secondary storage devices like disks and tapes and also gives insights on additional storage details.</i>
* Conceptual Level: <i>At conceptual level, data is represented in the form of various database tables. For Example, STUDENT database may contain STUDENT and COURSE tables which will be visible to users but users are unaware of their storage.Also referred as logical schema,it describes what kind of data is to be stored in the database.</i>
* External Level:  <i>An external level specifies a view of the data in terms of conceptual level tables.  Each external level view is used to cater to the needs of a particular category of users. For Example, FACULTY of a university is interested in looking course details of students, STUDENTS are interested in looking at all details related to academics, accounts, courses and hostel details as well. So, different views can be generated for different users. The main focus of external level is data abstraction.</i>

* <b>Data Independence: </b><i>Data independence means a change of data at one level should not affect another level. Two types of data independence are present in this architecture:</i><br>
  * Physical Data Independence: <i>Any change in the physical location of tables and indexes should not affect the conceptual level or external view of data. This data independence is easy to achieve and implemented by most of the DBMS.</i>
  * Conceptual Data Independence: <i>The data at conceptual level schema and external level schema must be independent. This means a change in conceptual schema should not affect external schema. e.g.; Adding or deleting attributes of a table should not affect the user’s view of the table. But this type of independence is difficult to achieve as compared to physical data independence because the changes in conceptual schema are reflected in the user’s view.</i>

* ## Two-tier architecture:
     The two-tier architecture is similar to a basic client-server model. The application at the client end directly communicates with the database at the server-side. APIs like ODBC, JDBC are used for this interaction. The server side is responsible for providing query processing and transaction management functionalities. On the client-side, the user interfaces and application programs are run. The application on the client-side establishes a connection with the server-side in order to communicate with the DBMS. 
An advantage of this type is that maintenance and understanding are easier, compatible with existing systems. However, this model gives poor performance when there are a large number of users. 

![image](https://user-images.githubusercontent.com/79071810/147412532-0aea3b5c-9e43-482d-ae10-cea05090e204.png)

* ## Three-tier architecture:
     In this type, there is another layer between the client and the server. The client does not directly communicate with the server. Instead, it interacts with an application server which further communicates with the database system and then the query processing and transaction management takes place. This intermediate layer acts as a medium for the exchange of partially processed data between server and client. This type of architecture is used in the case of large web applications. <br>
     
     <b> Advantages:</b>
     * <b>Enhanced scalability</b> due to distributed deployment of application servers. Now, individual connections need not be made between client and server.
     * <b>Data Integrity</b> is maintained. Since there is a middle layer between client and server, data corruption can be avoided/removed.
     * <b>Security</b> is improved. This type of model prevents direct interaction of the client with the server thereby reducing access to unauthorized data.
     
     <b>Disadvantages: </b>
     Increased complexity of implementation and communication. It becomes difficult for this sort of interaction to take place due to the presence of middle layers. 
     
     ![image](https://user-images.githubusercontent.com/79071810/147412605-6f4658bf-7314-4894-8b49-a79894db5527.png)

     

     
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
