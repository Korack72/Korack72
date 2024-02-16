
CREATE TABLE EMPLOYEE (
 EMP_CODE INT, EMP_NAME VARCHAR(20), DESIG VARCHAR(20), HEAD INT, DOB DATE,BASIC INT, DEPT_CODE INT, PRIMARY KEY ( EMP_CODE));

DESCRIBE EMPLOYEE;
-- insert
INSERT INTO EMPLOYEE VALUES (101, "Raju", "Manager", NULL, '2000-12-17', 8000, 20),
 (102, "Amar Roy", "Salesman", 105, '2000-02-20', 4000, 30),
 (103, "Raj", "Assistant", 101, '2003-02-22', 4500, 20),
 (104, "Rajiv Kumar", "As. Engineer", 107, '2001-04-02', 6200, 10),
 (105, "Suraj Patel", "Area Manager", NULL, '2001-09-28', 7500, 30),
 (106, "Binay Kumar", "Salesman", 105, '2001-05-01', 4270, 30),
 (107, "Ramaswamy", "Engineer", NULL, '2001-06-09', 6500, 10),
(108, "Joy Iyer", "Assistant", 105, '2002-12-09', 4250, 30),
 (109, "Imram Khan", "Steno", 105, '2001-11-17', 4500, 30),
 (110, "Tinu Anand", "As. Engineer", 107, '2003-01-12', 6000, 10);
 
SELECT * FROM EMPLOYEE

-----------------------------------------------------------------------------------------------------------------------------------
CREATE TABLE EMPLOYEE (
 EMP_CODE INT, EMP_NAME VARCHAR(20), DESIG VARCHAR(20), HEAD INT, DOB DATE,BASIC INT, DEPT_CODE INT, PRIMARY KEY ( EMP_CODE));

DESCRIBE EMPLOYEE;
-- insert
INSERT INTO EMPLOYEE VALUES (101, "Raju", "Manager", NULL, '2000-12-17', 8000, 20),
 (102, "Amar Roy", "Salesman", 105, '2000-02-20', 4000, 30),
 (103, "Raj", "Assistant", 101, '2003-02-22', 4500, 20),
 (104, "Rajiv Kumar", "As. Engineer", 107, '2001-04-02', 6200, 10),
 (105, "Suraj Patel", "Area Manager", NULL, '2001-09-28', 7500, 30),
 (106, "Binay Kumar", "Salesman", 105, '2001-05-01', 4270, 30),
 (107, "Ramaswamy", "Engineer", NULL, '2001-06-09', 6500, 10),
(108, "Joy Iyer", "Assistant", 105, '2002-12-09', 4250, 30),
 (109, "Imram Khan", "Steno", 105, '2001-11-17', 4500, 30),
 (110, "Tinu Anand", "As. Engineer", 107, '2003-01-12', 6000, 10);
 
 
SELECT * FROM EMPLOYEE ;
Select EMP_CODE, EMP_NAME, DEPT_CODE FROM EMPLOYEE order by DEPT_CODE;
Select * from employee order by DEPT_CODE DESC;



Select sum(BASIC) FROM EMPLOYEE;
Select sum(DEPT_CODE) FROM EMPLOYEE;

Select sum(BASIC) FROM EMPLOYEE where DEPT_CODE = 30; 

Select BASIC FROM EMPLOYEE where DEPT_CODE = 30; 



Select SUM(BASIC) FROM EMPLOYEE where  DESIG = 'Salesman';
Select MAX(BASIC) FROM EMPLOYEE where DEPT_CODE;
Select MIN(BASIC) FROM EMPLOYEE where DEPT_CODE;

Select MAX(BASIC) FROM EMPLOYEE where DEPT_CODE = 10;

Select COUNT(BASIC) FROM EMPLOYEE;
Select COUNT(*) FROM EMPLOYEE;


Select COUNT(DISTINCT DEPT_CODE) FROM EMPLOYEE;
Select COUNT(DEPT_CODE) FROM EMPLOYEE;

Select COUNT(DISTINCT HEAD) FROM EMPLOYEE;
Select COUNT(DEPT_CODE) FROM EMPLOYEE;

Select COUNT(BASIC) FROM EMPLOYEE where BASIC > 5000;
Select COUNT(BASIC) FROM EMPLOYEE where BASIC < 4500;

Select EMP_NAME, HEAD, DEPT_CODE FROM EMPLOYEE order by DEPT_CODE
----------------------------------------------------------------------------------------------------------------------------------


delete from EMPLOYEE where EMP_CODE = 105;
Select * from EMPLOYEE;

-- AVERAGE 
Select avg(BASIC)FROM EMPLOYEE where EMP_CODE;
select DEPT_CODE,sum(BASIC),COUNT(DEPT_CODE)from EMPLOYEE group by DEPT_CODE;
--------------------------------------------------------------------------------------------------------------------------------------------


create table ravan(Std_ID int,name varchar(45),address varchar(56),gender char(45),dob date,fees float ,primary key(Std_id));
describe ravan;
insert into ravan values(1,'Rahul','Mandi','Male','2000-12-17','8000'),(2,'Amar roy','Delhi','Male','2000-02-20','4000'),
(3,'Ram','Sunder Nagar','Male','2002-05-01','5000'),(4,'Yash','Mumbai','Male','2003-12-09','9000'),
(5,'Naveen','Kangra','Male','2002-01-05','5000'),(6,'Rohit','Kangoo','Male','2004-12-09','6000'),
(7,'Nikhil','Lahul spiti','Male','2002-11-05','7000'),(8,'Krishna','Nihri','Male','2005-01-15','10000'),
(9,'Laksman','kullu','Male','2000-11-05','8000'),(10,'kapil','Barmana','Male','2001-04-09','15000'),
(11,'kartik','Shimla','Male','2005-06-13','12000');
select*from ravan;
set autocommit=0;
insert into ravan value(12, 'Vishal', 'Bilashpur', 'Male', '1998-01-27', '10000');
select * from ravan;
rollback; 
select *from ravan;

set autocommit=1;
insert into ravan value(12, 'Vishal', 'Bilaspur', 'Male', '1998-01-27', '10000');
select * from ravan;
rollback;
select*from ravan;

set autocommit =1;
update ravan set name='Vinod' where Std_ID=6;
update ravan set address='Kinaur' where Std_ID=5;
update ravan set fees=10000 where Std_ID=5;
select*from ravan;
rollback;
select*from ravan;

set autocommit =1;
update ravan set name='amir' where Std_ID=5;
update ravan set address='Japan' where Std_ID=5;
update ravan set fees=10000 where Std_ID=5;
select*from ravan;
rollback;
select*from ravan;
--------------------------------------------------------------------------------------------------------------------------------------------

create table Person(Std_ID int,name varchar(45),gender char(45),dob date,fees float ,primary key(Std_id));
describe Person;
insert into Person values
(1,'Rahul','Male','2000-12-17','8000'),
(2,'Amar roy','Male','2000-02-20','4000'),
(3,'Ram','Male','2002-05-01','5000'),
(4,'Yash','Male','2003-12-09','9000'),
(5,'Naveen','Male','2002-01-05','5000'),
(6,'Rohit','Male','2004-12-09','6000'),
(7,'Nikhil','Male','2002-11-05','7000');

select min(dob) from Person;
select max(dob) from Person;
select DAYNAME('2024-02-15');
select*from Person;
------------------------------------------------------------------------------------------
