# Image Design of a Railway Database Management System
A database is key to every software. Database is a collection of interrelated data which helps in the efficient retrieval, insertion, and deletion of data from the database and organizes the data in the form of tables, views, schemas, reports, etc. For example, a railway database organizes the data about trains, passengers, stations, tickets, schedule, routes, admin staff, etc. which helps in the efficient retrieval, insertion, and deletion of data from it.

## Database Management System
A Database Management System (DBMS) is a software system that is designed to manage and organize data in a structured manner. It allows users to create, modify, and query a database, as well as manage the security and access controls for that database. DBMS can be classified into two types: Relational Database Management System (RDBMS) and Non-Relational Database Management System (NoSQL or Non-SQL). In RDBMS the data is organized in the form of tables and each table has a set of rows and columns. The data is related to each other through primary and foreign keys.

MySQL, Oracle, etc. are popular commercial DBMS used in different applications.

## Storing an Image
All data is stored as its own datatype in a database. In the case of a name we use the datatype varchar. In the case of an image we use the datatype BLOB, which stands for Binary Large Object. BLOB is a collection / chunk of binary data stored in the form of a single entity in a database system. BLOBs primarily hold images, videos, sound, and other multimedia objects.

## Image Design
In MySQL, there are actually three flavors of BLOB. The one you choose depends on the size of the images that you will be storing. If in doubt, go to the larger capacity BLOB. Here are the three BLOB types:
* BLOB: Can handle up to 65,535 bytes of data (65 KB).
* MEDIUMBLOB: The maximum length supported is 16,777,215 bytes (16.7 MB).
* LONGBLOB: Stores up to 4,294,967,295 bytes of data (4.29 GB).

```
CREATE TABLE images (
image_id tinyint
image_name varchar
image blob
);
```

This is SQL code for creating the images table in the database with different image types as columns.
Here is a screenshot of the table in the database:

![Image](https://i.ibb.co/JrPFN6J/table-def.jpg)

## Criminology action
In our railway scenario, we would like to store the image of the passenger. In case of an alarm one can quickly identify the crook by sharing all his data with public authority like the police. With passenger photo, the police can ask the general public for help.
