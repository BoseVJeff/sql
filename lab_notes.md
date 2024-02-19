Data types:
* char - 0-255 => small data (eg. yes/no)
* varchar - upto 2000
* varchar2 - upto 4000/2GB

Create table:
```sql
CREATE TABLE studentb (
    rno NUMBER(5),
    sname VARCHAR2(15)
);
```

Add records:
Three methods:

1. First Method

```sql
INSERT INTO studentb VALUES (1, 'abc');
```

> Five records were inserted as a part of this exercise.

Display all records from Table
```sql
SELECT * FROM studentb;
```

Displays data in tabular form.

Display column(s) from table
```sql
SELECT sname FROM studentb;
```

```sql
SELECT rno,sname FROM studentb;
```

> Seperate multiple column names using a `,`.

Delete record
```sql
DELETE FROM studentb WHERE rno=2;
```

Get unique records
```sql
SELECT DISTINCT(Id) from table;
```

## Exercise
```sql
CREATE TABLE EMPLOYEES (
    Employee_id NUMBER(6),
    First_Name VARCHAR2(20),
    Last_Name VARCHAR(20),
    Email VARCHAR(15),
    Phone_Number NUMBER(12),
    Hire_Date DATE,
    Job_Id NUMBER(6),
    Salary NUMBER(10),
    Commission_Pct NUMBER(3),
    Manager_Id NUMBER(6),
    Department_Id NUMBER(6)
);\
```


```sql
INSERT INTO EMPLOYEES VALUES (1, 'first', 'first', 'first@mail.com', 132456798, '12-jan-24', 2, 123456, 10, 1,1);
INSERT INTO EMPLOYEES VALUES (2, 'second', 'sec', 'sec@mail.com', 1324567498, '11-jan-24', 3, 1234565, 10, 1, 1);
INSERT INTO EMPLOYEES VALUES (3, 'th', 'th', 'third@mail.com', 152456798, '10-jan-24', 2, 1234526, 10, 1, 2);
INSERT INTO EMPLOYEES VALUES (4, 'four', 'four', 'four@mail.com', 14332456798, '09-jan-24', 3, 127456, 10, 2, 1);
INSERT INTO EMPLOYEES VALUES (5, 'fifth', 'fifth', 'fifth@mail.com', 134456798, '08-jan-24', 2, 1234568, 10, 2, 2);
```

* Find out employee id, names, salaries of all the employees

* List out all employees who works under manager 100

* Find the names of the employees who have a salary greater than or equal to 4800

* Find the names of employees whose last name is "AUSTIN"

* Find the names of the employees who works in departments 60, 70, and 80

* Display the unique Manager_Id

## Exercise

```sql
CREATE TABLE employees (
    id NUMBER,
    first_name VARCHAR2(20),
    last_name VARCHAR2(20),
    department VARCHAR(20),
    salary NUMBER(6,2)
);

INSERT INTO employees VALUES(1, 'Paul', 'Garrix', 'Corporate', 3547.25);
INSERT INTO employees VALUES(2, 'Astrid', 'Fox', 'Private Individuals', 2845.56);
INSERT INTO employees VALUES(3, 'Matthias', 'Johnson', 'Private Individuals', 3009.41);
INSERT INTO employees VALUES(4, 'Lucy', 'Patterson', 'Private Individuals', 3547.25);
INSERT INTO employees VALUES(5, 'Tom', 'Page', 'Corporate', 5974.41);
INSERT INTO employees VALUES(6, 'Claudia', 'Conte', 'Corporate', 4717.12);
INSERT INTO employees VALUES(7, 'Walter', 'Deer', 'Private Individuals', 3547.25);
INSERT INTO employees VALUES(8, 'Stephanie', 'Marx', 'Corporate', 2894.51);
INSERT INTO employees VALUES(9, 'Luca', 'Pavarotti', 'Private Individuals', 4123.45);
INSERT INTO employees VALUES(10, 'Victoria', 'Pollock', 'Corporate', 4789.53);
```

1. Show the structure of the table
```sql
DESC employees;
```

2. Display all rows in table
```sql
SELECT * FROM employees;
```

3. Display first name and last name of table
```sql
SELECT first_name, last_name FROM employees;
```

4. Display name of employee whose department is 'Corporate'
```sql
SELECT first_name, last_name FROM employees WHERE department='Corporate';
```

5. Display first and last name of employee whose first name is 'Victoria'
```sql
SELECT first_name, last_name FROM employees WHERE first_name='Victoria';
```

6. Display forst and last name of employee last name should be in ascending order
```sql
SELECT first_name, last_name FROM employees ORDER BY last_name ASC;
```
> Note that `ASC` can be omitted as it is the default option.

7. Display first and last name of employee first name should be in descending order
```sql
SELECT first_name, last_name FROM employees ORDER BY first_name DESC;
```

## Exercise

Create table `EMPLOYEES` with the following columns:
* Employee_Id
* First_Name
* Last_Name
* Email
* Phone_Number
* Hire_Date
* Job_Id
* Salary
* Commision_Pct
* Manager_Id
* Department_Id

1. Find employee id, names, and salaries of all employees.
2. List employees who work under manager 100

## Lab 03

```sql
CREATE TABLE client_master(
    client_no NUMBER(3),
    name VARCHAR2(10),
    address1 VARCHAR2(15),
    address2 VARCHAR2(15),
    city VARCHAR2(10),
    pincode NUMBER(6),
    bal_due NUMBER(6)
);
```


```sql
INSERT INTO client_master VALUES (001, 'J Doe', '123 Main St.','Apt. 1', 'Bombay', 400012, 2800);
INSERT INTO client_master VALUES (002, 'J Smith', '456 Elm St.', 'Apt. 2', 'Delhi', 110001, 3200);
INSERT INTO client_master VALUES (003, 'M Jones', '789 Oak St.', 'Apt. 3', 'Chennai', 600001, 3000);
INSERT INTO client_master VALUES (004, 'M Johnson', '1011 Pine St.', 'Apt. 4', 'Banglore', 560001, 2900);
INSERT INTO client_master VALUES (005, 'R Brown', '1213 Maple St.', 'Apt. 5', 'Hyderabad', 500001, 3100);
```

```sql
CREATE TABLE product_master(
    pno NUMBER(3),
    description VARCHAR2(25),
    profit_percent NUMBER(3),
    unit_measure NUMBER(5),
    quantity NUMBER(5),
    sell_price NUMBER(10),
    cost_price NUMBER(10)
);
```

###SQLite

```sql
CREATE TABLE client_master (
client_no INTEGER(3),
name TEXT(25),
address1 TEXT(25),
adress2 TEXT(25),
city TEXT(25),
pincode TEXT(6),
state TEXT(25),
bal_due REAL(5)
);
```

```sql
INSERT INTO client_master VALUES (001, 'J Doe', '123 Main St.','Apt. 1', 'Bombay', 400012, 'Maharashtra', 2800);
INSERT INTO client_master VALUES (002, 'J Smith', '456 Elm St.', 'Apt. 2', 'Delhi', 110001,'Delhi', 3200);
INSERT INTO client_master VALUES (003, 'M Jones', '789 Oak St.', 'Apt. 3', 'Chennai', 600001,'Tamil Nadu', 3000);
INSERT INTO client_master VALUES (004, 'M Johnson', '1011 Pine St.', 'Apt. 4', 'Banglore', 560001,'Karnataka', 2900);
INSERT INTO client_master VALUES (005, 'R Brown', '1213 Maple St.', 'Apt. 5', 'Hyderabad', 500001,'Andhra Pradesh', 3100);
```

```sql
CREATE TABLE product_master (
pno INTEGER(3),
description TEXT(50),
profit_precent REAL(5),
unit_measure INTEGER(5),
quantity INTEGER(5),
sell_price REAL(10),
cost_price REAL(10)
);
```

```sql
INSERT INTO product_master VALUES
(001, 'Product 1 is nice', 0.25, 5, 75, 3200, 3000),
(002, 'Product 2 is good', 0.15, 5, 100, 3200, 3000),
(003, 'Product 3 is okay', 0.25, 5, 35, 3200, 3000),
(004, 'Product 4 is bad', 0.25, 5, 15, 3200, 3000),
(005, 'Product 5 is terrible', 0.25, 5, 75, 3200, 3000);
```

```sql
CREATE TABLE salesman_master (
smno INTEGER(3),
sname TEXT(25),
address1 TEXT(25),
adress2 TEXT(25),
city TEXT(25),
pincode TEXT(6),
state TEXT(25),
sal_amount REAL(5),
target_no INTEGER(5),
ytd_sale INTEGER(5),
remarks TEXT(50)
);
```

```sql
INSERT INTO salesman_master VALUES
(001, 'J Ohn', 'Ap 1', 'New St', 'Banglore', 125354, 'Karnataka', 2500, 100, 56, "None"),
(001, 'H Arry', 'Ap 2', 'Another New St', 'Coimbatore', 125354, 'Tamil Nadu', 4000, 90, 46, "None"),
(001, 'M Ike', 'Ap 3', 'Yet Another New St', 'Kolkata', 125354, 'West Bengal', 3000, 100, 56, "None"),
(001, 'W ebster', 'Ap 4', 'Wow A New St', 'Delhi', 125354, 'Delhi', 3500, 100, 56, "None"),
(001, 'R Honda', 'Ap 5', 'What A New St', 'Ahemdabad', 125354, 'Gujarat', 3500, 100, 56, "None");
```

```sql
SELECT name FROM client_master;
```

```sql
 SELECT * FROM client_master;
```

```sql
UPDATE client_master SET "city"='Bombay' WHERE "client_no"=005;
```

```sql
SELECT name, city FROM client_master;
```

```sql
SELECT pno FROM product_master;
```

```sql
SELECT name, city FROM client_master WHERE city="Bombay";
```

```sql
SELECT sname, sal_amount FROM salesman_master WHERE sal_amount=3000;
```

```sql
UPDATE client_master SET bal_due=10000 WHERE client_no=001;
```

```sql
UPDATE salesman_master SET city="Mumbai";
```

```sql
DELETE FROM salesman_master WHERE sal_amount=3500;
```

```sql
DELETE FROM product_master WHERE quantity=100;
```

```sql
DELETE FROM client_master WHERE city='Tamil Nadu';
```

```sql
ALTER TABLE client_master ADD COLUMN 'telephone' TEXT(15);
```

```sql

```

-----

Create table Employee with the following fields:

|Name|Type|
|----|----|
|Empno|Number|
|Ename|Varchar2(20)|
|Job|Varchar2(20)|
|Mgr|Number|
|Sal|Number|

```sql
CREATE TABLE Employee (
    Empno Number,
    Ename VARCHAR2(20),
    Job VARCHAR2(20),
    Mgr Number,
    Sal Number
);
```


* Insert any five records into the table

```sql
INSERT INTO Employee VALUES (12, 'John Doe', 'Developer', 8,3000);
INSERT INTO Employee VALUES (12, 'Wen Doe', 'HR', 4,3500);
INSERT INTO Employee VALUES (12, 'Sales Man', 'Sales', 3,4000);
INSERT INTO Employee VALUES (12, 'Holliday Day', 'Manager', 2,6000);
INSERT INTO Employee VALUES (12, 'Webber Sing', 'Web Admin', 4,2000);
```


* Add a column Deptno with domain to the Employee table

```sql
ALTER TABLE Employee ADD (Deptno NUMBER);
```

* Update the column details of Job to 25

```sql
ALTER TABLE Employee MODIFY (Job VARCHAR2(25));
```


* Rename the column of emp_name of Employ

```sql
ALTER TABLE Employee RENAME COLUMN Empno TO Employ;
```


* Delete the employee whose empno is 19

```sql
DELETE FROM Employee WHERE Employ=19;
```

------
Create department table with the following structure:

|Name|Type|
|----|----|
|Deptno|Number|
|Deptname|Varchar2(30)|
|location|Varchar2(20)|

```sql
CREATE TABLE department (
    Deptno Number,
    Deptname Varchar2(30),
    location Varchar(20)
);
```


* Insert values into the table

```sql
INSERT INTO department VALUES (01, 'Department of Azerty', 'Azerty');
INSERT INTO department VALUES (02, 'Department of Qwerty', 'Qwerty');
INSERT INTO department VALUES (03, 'Department of Zxcvbn', 'Zxcvbn');
INSERT INTO department VALUES (04, 'Department of Azerty', 'Zxcvbn');
INSERT INTO department VALUES (05, 'Department of Zxcvbn', 'Azerty');
```

* Add column designation to department

```sql
ALTER TABLE department ADD (designation VARCHAR2(20));
```

* List the records of emp table grouped by deptno

* Update the deptno with Testester record where deptno is 9

```sql
UPDATE DEPARTMENT SET Deptname='Testester' WHERE Deptno=9;
```

* Delete deptname column from the table

```sql
ALTER TABLE department DROP COLUMN Deptname;
```

------
Create table called Customer

|Name|Type|
|----|----|
|Cust name|Varchar2(30)|
|Cust street|Varchar2(20)|
|Cust city|Varchar2(30)|

```sql
CREATE TABLE Customer (
    Cust_name Varchar2(20),
    Cust_street Varchar2(20),
    Cust_city Varchar2(20)
);
```


* Insert records into the table

```sql
INSERT INTO Customer VALUES ('John Doe', 'High Street', 'Hightown');
INSERT INTO Customer VALUES ('Jo Odo', 'China Street', 'Chinatown');
INSERT INTO Customer VALUES ('Mousie Mouser', 'Low Street', 'Lowtown');
INSERT INTO Customer VALUES ('Norma Norman', 'Mid Street', 'Midtown');
INSERT INTO Customer VALUES ('J P Peter', 'High Street', 'Hightown');
```

* Add salary column to the table

```sql
ALTER TABLE Customer ADD (Salary NUMBER);
```

* Alter the table column street with 25

```sql
ALTER TABLE Customer MODIFY (Cust_street VARCHAR2(25));
```

* Drop salary column of customer table
* Delete the rows of customer tabe whose cust_city is "hydrabad"

## Notes 08/02

```sql
sid number(3) references b1;
```

Primary keys *cannot* be deleted of any of the child table references it. The child items *must* be deleted first. This is also true for the tables themselves.

To automatically delete relevant records, use `cascade`.

```sql
sid number(3) references b1 on delete cascade;
```

Cascade discussion for other options [on SE](https://dba.stackexchange.com/a/213239).

## Exercise

```sql
CREATE TABLE tbl_salesman (
    salesman_id NUMBER(4) PRIMARY KEY,
    name VARCHAR2(10),
    city VARCHAR2(8),
    commission NUMBER(3,2)
);

CREATE TABLE tbl_customer (
    customer_id NUMBER(4) PRIMARY KEY,
    customer_name VARCHAR2(12),
    city VARCHAR2(10),
    grade NUMBER(3),
    salesman_id NUMBER(4) REFERENCES tbl_salesman ON DELETE CASCADE
);

CREATE TABLE tbl_order (
    order_no NUMBER(5) PRIMARY KEY,
    purch_amt NUMBER(6,2),
    order_date DATE,
    customer_id NUMBER(4) REFERENCES tbl_customer ON DELETE CASCADE,
    salesman_id NUMBER(4) REFERENCES tbl_salesman ON DELETE CASCADE
);
```

```sql
INSERT INTO tbl_salesman VALUES (5001, 'James Hoog', 'New York', 0.15);
INSERT INTO tbl_salesman VALUES (5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO tbl_salesman VALUES (5005, 'Pit Alex', 'London', 0.11);
INSERT INTO tbl_salesman VALUES (5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO tbl_salesman VALUES (5003, 'Lauson Hen', NULL, 0.12);
INSERT INTO tbl_salesman VALUES (5007, 'Paul Adam', 'Rome', 0.13);


INSERT INTO tbl_customer VALUES (3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO tbl_customer VALUES (3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO tbl_customer VALUES (3001, 'Brad Guhan', 'London', NULL, NULL);
INSERT INTO tbl_customer VALUES (3004, 'Fabian Johns', 'Paris', 300, 5006);
INSERT INTO tbl_customer VALUES (3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO tbl_customer VALUES (3009, 'Geoff Camero', 'Berlin', 100, NULL);
INSERT INTO tbl_customer VALUES (3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO tbl_customer VALUES (3003, 'Jozy Altidor', 'Moncow', 200, 5007);


INSERT INTO tbl_order VALUES (70001, 150.5, '05-oct-2016', 3005, 5002);
INSERT INTO tbl_order VALUES (70009, 270.65, '10-sep-2016', 3001, NULL);
INSERT INTO tbl_order VALUES (70002, 65.26, '05-oct-2016', 3002, 5001);
INSERT INTO tbl_order VALUES (70004, 110.5, '17-aug-2016', 3009, NULL);
INSERT INTO tbl_order VALUES (70007, 948.5, '10-sep-2016', 3005, 5002);
INSERT INTO tbl_order VALUES (70005, 2400.6, '27-jul-2016', 3007, 5001);
INSERT INTO tbl_order VALUES (70008, 5760, '10-sep-2016', 3002, 5001);
INSERT INTO tbl_order VALUES (70010, 1983.43, '10-oct-2016', 3004, 5006);
INSERT INTO tbl_order VALUES (70003, 2480.4, '10-oct-2016', 3009, NULL);
INSERT INTO tbl_order VALUES (70012, 250.45, '27-jun-2016', 3008, 5002);
INSERT INTO tbl_order VALUES (70011, 75.29, '17-aug-2016', 3003, 5007);
```

* Display name and commision of all the salesmen

```sql
SELECT name, commission FROM tbl_salesman;
```

* Retrieve salesman id of all salesmen from orders table

```sql
SELECT DISTINCT(salesman_id) FROM tbl_salesman;
```

* Display names and city of all salesmen from orders table without any repeats

```sql
SELECT DISTINCT(salesman_id) FROM tbl_order;
```

* Display names and city of salesman who belongs to the city of Paris

```sql
SELECT name, city FROM tbl_salesman WHERE city='Paris';
```

* Display all information for those customers with a grade of 200

```sql
SELECT * FROM tbl_customer WHERE grade=200;
````

* Display the order number, order date and the purchase amount for order(s) which will be delivered by the salesman with ID 5001

* Display all details of customers whose name starts with nick

```sql
SELECT * FROM tbl_customer WHERE customer_name LIKE 'Nick%';
```

* Display all details of customers whose name is not start with B

```sql
SELECT * FROM tbl_customer WHERE customer_name NOT LIKE 'B%';
```

* Display all customers who either belong to city of new york or had a grade over 100

```sql
SELECT * FROM tbl_customer WHERE city='New York' OR grade>100;
```

* Find all information of salesmen whose commisiion is between 0.12 and 0.14

```sql
SELECT * FROM tbl_salesman WHERE commission>0.12 and commission<0.14;
```

```sql
SELECT * FROM tbl_salesman WHERE commission BETWEEN 0.12 and 0.14;
```

* Find all customers whose names are ending with the letter n

```sql
SELECT * FROM tbl_customer WHERE customer_name LIKE '%n';
```

* Find those salesmen with all information whose name contains 1st character N, 4th character 'l' and rest may be any character

```sql
SELECT * FROM tbl_salesman WHERE name LIKE 'N__l%';
```

* Find that customer whith all information who doesnot get any grade except NULL

```sql
SELECT * FROM tbl_customer WHERE grade IS NOT NULL;
```

* Find total purchase amount of all orders

```sqlSELECT SUM(purch_amt) FROM tbl_order;
```

> ```sql
> SELECT AVG(purch_amt) FROM tbl_order;
> ```
> for average

> Row-wise addition
>
> ```sql
> SELECT s1, s2, s1+s2 as total FROM res;
> ```

> Row-wise operations
>
> ```sql
> SELECT UPPER(city) from s1;
> SELECT LOWER(city) from s1;
> SELECT INITCAP(city) from s1;
> ```

* Find the number of salesman currently listing for all their customers
```sql
SELECT COUNT(DISTINCT(salesman_id)) FROM tbl_order;
```

* Find the highest grade for each of the cities of customers
> `GROUP BY` requires atleast one aggregrate query
>
> ```sql
> SELECT city,MAX(grade) FROM tbl_customer GROUP BY city;
> ```

> `SUM`, etc can also be used

> `HAVING` is only used with `GROUP BY` to apply condition on the result of `GROUP BY`
>
> ```sql
> SELECT city, MAX(grade) FROM tbl_customer GROUP BY city HAVING MAX(grade) >= 200;
> ```

* Find highest purchase amount ordered by each customer on a particular date with their ID, order date and highest purchase amount

```sql
SELECT customer_id, order_date, MAX(purch_amt) from tbl_order GROUP BY customer_id, order_date;
```

* Find the highest purchase amount on a date `2012-08-17` for each salesman with their ID.

```sql
SELECT salesman_id, MAX(purch_amt) FROM tbl_order WHERE order_date='17-aug-2012' GROUP BY salesman_id;
```

* Find the highest purchase amount with their customer ID and order date, for only those customers who have the highest purchase amount in a day is more than 2000

```sql
SELECT customer_id, order_date ,MAX(purch_amt) FROM tbl_order GROUP BY customer_id, order_date HAVING MAX(purch_amt) > 2000;
```

* Write a SQL statement that counts all orders for a date August 17th, 2016

```sql
SELECT COUNT(order_no) FROM tbl_order WHERE order_date='17-Aug-2016';
```

* Find the name and city of those customers and salesman who lives in the same city

```sql
SELECT tbl_salesman.name, tbl_customer.customer_name, tbl_customer.city FROM tbl_salesman, tbl_customer WHERE tbl_salesman.city=tbl_customer.city;
```

* Find names of all customers along with the salesmen who works for them

```sql
SELECT tbl_customer.customer_name, tbl_salesman.name FROM tbl_customer, tbl_salesman WHERE tbl_customer.salesman_id=tbl_salesman.salesman_id;
```

* Display all those orders by the customer not located in the same cities where their salesmen live

```sql
SELECT tbl_order.order_no, tbl_salesman.name, tbl_salesman.city, tbl_customer.customer_name, tbl_customer.city FROM tbl_order, tbl_salesman, tbl_customer WHERE tbl_salesman.city<>tbl_customer.city AND tbl_order.salesman_id=tbl_salesman.salesman_id AND tbl_order.customer_id=tbl_customer.customer_id;
```

* Display all the orders issued by the salesman 'Paul Adam' from the orders table

```sql
SELECT * FROM tbl_order WHERE salesman_id=(SELECT salesman_id FROM tbl_salesman WHERE name='Paul Adam');
```

* Display all the orders whose values are greater than the average order value for 10th October 2016

```sql
SELECT * FROM tbl_order WHERE purch_amt > (SELECT AVG(purch_amt) FROM tbl_order WHERE order_date='10-October-2016');
```

* Find all orders attributed to salesmen in Paris

```sql
SELECT * FROM tbl_order WHERE salesman_id IN (SELECT salesman_id FROM tbl_salesman WHERE city='Paris');
```

* Display customer name in upper case

```sql
SELECT UPPER(customer_name) FROM tbl_customer;
```

* Display max and min purchase amount from table

```sql
SELECT MAX(purch_amt) AS maximum_balance, MIN(purch_amt) AS minimum_balance FROM tbl_order;
```

* Display salesman name in init-cap

```sql
SELECT INITCAP(name) FROM tbl_salesman;
```