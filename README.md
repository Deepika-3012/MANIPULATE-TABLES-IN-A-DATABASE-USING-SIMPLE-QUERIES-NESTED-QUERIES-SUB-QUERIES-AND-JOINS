# MANIPULATE-TABLES-IN-A-DATABASE-USING-SIMPLE-QUERIES-NESTED-QUERIES-SUB-QUERIES-AND-JOINS
AIM:

To create simple queries,nested queries,subqueries and joins using tables.

PROCEDURE:

STEP 1: Start the program.

STEP 2: Create two different tables with its essential attributes.

STEP 3: Insert attribute values into the table.

STEP 4: Create the Nested query and join from the above created table.

STEP 5: Execute Command and extract information from the tables.

STEP 6: Stop the program.

COMMANDS:

NESTED QUERY

SQL>create table student(id number(10), name varchar2(20),classID number(10), marksvarchar2(20));

SQL>insert into student values(1,'pinky',3,2.4);

SQL>insert into student values(2,'bob',3,1.44);

SQL>insert into student values(3,'Jam',1,3.24);

SQL>insert into student values(4,'lucky',2,2.67);

SQL>insert into student values(5,'ram',2,4.56);

SQL>select * from student;

SQL>Create table teacher(id number(10), name varchar(20), subject varchar2(10), classIDnumber(10), salary number(30));

SQL>insert into teacher values(1,’bhanu’,’computer’,3,5000);

SQL>insert into teacher values(2,'rekha','science',1,5000);

SQL>insert into teacher values(3,'siri','social',NULL,4500);

SQL>insert into teacher values(4,'kittu','mathsr',2,5500);

SQL>select * from teacher;

SQL>Create table class(id number(10), grade number(10), teacherID number(10),noofstudents number(10));

SQL>insert into class values(1,8,2,20);

SQL>insert into class values(2,9,3,40);

SQL>insert into class values(3,10,1,38);

SQL>select * from class;

SQL> Select AVG(noofstudents) from class where teacherID IN(Select id from teacher Where subject=’science’ OR subject=’maths’);

SQL> SELECT * FROM student WHERE classID = ( SELECT id FROM class WHERE2 noofstudents = ( SELECT MAX(noofstudents) FROM class));

JOINS:

EQUIJOIN.

SQL> SELECT ID, NAME, AMOUNT, DATE FROM CUSTOMERS INNER JOIN

ORDERS ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;

LEFT JOIN

SQL> SELECT ID, NAME, AMOUNT, DATE FROM CUSTOMERS LEFT JOIN

ORDERS ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;

RIGHT JOIN

SQL> SELECT ID, NAME, AMOUNT, DATE FROM CUSTOMERS RIGHT JOIN ORDERS ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;

FULL JOIN

SQL> SELECT ID, NAME, AMOUNT, DATE FROM CUSTOMERS FULL JOIN ORDERS ON CUSTOMERS.ID = ORDERS.CUSTOMER_ID;

SELF JOIN:

SQL> SELECT a.ID, b.NAME, a.SALARY FROM CUSTOMERS a, CUSTOMERS b WHERE a.SALARY < b.SALARY;

CARTESIAN JOIN :

SQL> SELECT ID, NAME, AMOUNT, DATE FROM CUSTOMERS, ORDERS;

RESULT:

Thus the simple queries, nested queries ,sub queries and joins has been executed successfully.
