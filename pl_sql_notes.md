* Simple Output

    ```sql
    BEGIN
    dbms_output.put_line('Hello World!');
    END;
    ```

* Variables

    ```sql
    DECLARE
    txt1 VARCHAR2(30);
    BEGIN
    txt1:='Hello';
    dbms_output.put_line(txt1);
    END;
    ```

> User input is supported using the standard `&desc`.

* String Concatenation

    ```sql
    DECLARE
    txt1 VARCHAR2(30);
    BEGIN
    txt1:='Hello';
    dbms_output.put_line('The string is ' || txt1);
    END;
    ```

* Numbers

    ```sql
    DECLARE
    txt1 VARCHAR2(30);
    a NUMBER(3);
    b INTEGER;
    c int;
    BEGIN
    txt1:='Hello';
    a:=10;
    b:=20;
    c:=30;
    dbms_output.put_line('The string is ' || txt1);
    dbms_output.put_line('The value of a is ' || a);
    dbms_output.put_line('The value of b is ' || b);
    dbms_output.put_line('The value of c is ' || c);
    END;
    ```

* Perform arithmetic operations using PL/SQL
* Swap, in PL/SQL, two variables with and without a third variable.

```sql
DECLARE
a NUMBER(3);
b NUMBER(3);
c NUMBER(3);
BEGIN
a:=10;
b:=20;
dbms_output.put_line('The value of a is ' || a);
dbms_output.put_line('The value of b is ' || b);
c:=a+b;
dbms_output.put_line('a+b='||c);
c:=a-b;
dbms_output.put_line('a-b='||c);
c:=a*b;
dbms_output.put_line('a*b='||c);
c:=a/b;
dbms_output.put_line('a/b='||c);

dbms_output.put_line('Swapping using third variable...');
c:=a;
a:=b;
b:=c;
dbms_output.put_line('The value of a is ' || a);
dbms_output.put_line('The value of b is ' || b);

dbms_output.put_line('Swapping without third variable...');
a:=a-b;
b:=a+b;
a:=b-a;
dbms_output.put_line('The value of a is ' || a);
dbms_output.put_line('The value of b is ' || b);
END;
```

* Area of circle

```sql
DECLARE
r NUMBER;
ar NUMBER;
pi NUMBER;
BEGIN
pi:=3.14;
r:=10;
ar:=pi*POWER(r,2);
dbms_output.put_line('Area is '||ar);
END;
```

* Cube of number

```sql
DECLARE
a NUMBER;
r NUMBER;
BEGIN
a:=10;
r:=POWER(a,3);
dbms_output.put_line('Cube of '|| a ||' is ' || r);
END;
```

* For Loop

```sql
DECLARE
a NUMBER;
BEGIN
FOR a in 1..10 LOOP
dbms_output.put_line('Value of a is '||a);
END LOOP;
END;
```

`If` conditions: `IF...THEN...END IF`, `IF...THEN...ELSE...END IF`, `IF...THEN...ELSIF...THEN...ELSE...END IF`

* Check if number is positive, negative, or zero

```sql
DECLARE
a NUMBER;
BEGIN
a:=5;
IF a>0 THEN
dbms_output.put_line('+ve');
ELSIF a<0 THEN
dbms_output.put_line('-ve');
ELSE
dbms_output.put_line('zero');
END IF;
END;
```

* Input a number and check if number is even or odd

```sql
DECLARE
a NUMBER;
BEGIN
a:=10;
IF MOD(a,2)=0 THEN
dbms_output.put_line('Even');
ELSE
dbms_output.put_line('Odd');
END IF;
END;
```

* Input three numbers and find the maximum among them

```sql
DECLARE
n1 NUMBER;
n2 NUMBER;
n3 NUMBER;
BEGIN
n1:=10;
n2:=20;
n3:=15;
IF n1>=n2 THEN
    IF n1>=n3 THEN
    dbms_output.put_line('n1 is largest');
    END IF;
ELSIF n2>=n3 THEN
    IF n2>=n1 THEN
    dbms_output.put_line('n2 is largest');
    END IF;
ELSE
dbms_output.put_line('n3 is largest');
END IF;
END;
```

* Perform arithmetic calculator using menu

* Input age and display of person is eligible for voting or not.

* Input a character and display if character is vowel or consonant.

* Basic Loop

```sql
DECLARE
    i int;
BEGIN
    i:=1;
    LOOP
        IF i>10 THEN
            EXIT;
        END IF;
        dbms_output.put_line(i);
        i:=i+1;
    END LOOP;
END;
```

* Print even numbers using loops from 2 to 10

```sql
DECLARE
    i int;
BEGIN
    i:=0;
    LOOP
        i:=i+2;
        dbms_output.put_line(i);
        EXIT WHEN i>=10;
    END LOOP;
END;
```

* Print numbers from 1 to 10 using `while` loop

```sql
DECLARE
	i int;
BEGIN
	i:=1;
	WHILE i<=10 LOOP
		dbms_output.put_line(i);
		i:=i+1;
	END LOOP;
END;
```

* Print numbers from 1 to 10 and from 10 to 1 using `for` loop

```sql
DECLARE
a NUMBER;
BEGIN
FOR a in 1..10 LOOP
dbms_output.put_line(a);
END LOOP;
FOR a in REVERSE 1..10 LOOP
dbms_output.put_line(a);
END LOOP;
END;
```

* Print first 100 even numbers using `while` and `for` loops

```sql
DECLARE
num int;
cnt int;
BEGIN
num:=2;
FOR cnt IN 1..100 LOOP
dbms_output.put(num||' ');
num:=num+2;
END LOOP;
dbms_output.new_line;
END;
```

```sql
DECLARE
    num int;
    cnt int;
BEGIN
    cnt:=0;
    num:=2;
    WHILE cnt<100 LOOP
        dbms_output.put_line(num);
        cnt:=cnt+1;
        num:=num+2;
    END LOOP;
END;
```

* Implement Fibonacci series

```sql
DECLARE
n1 int;
n2 int;
n3 int;
cnt int;
BEGIN
cnt:=10;
n1:=0;
n2:=1;
dbms_output.put_line(n1);
FOR i IN 1..cnt LOOP
dbms_output.put_line(n2);
n3:=n1+n2;
n1:=n2;
n2:=n3;
END LOOP;
END;
```

* Sequences

> Syntax
>
> ```sql
> CREATE SEQUENCE <sequence_name>
> START WITH 1
> INCREMENT BY 1
> MINVALUE 1
> MAXVALUE 100;
> ```

* Create a table with roll number and name fields. Enter 10 values using a sequence.

```sql
CREATE TABLE tbl1 (
    rno NUMBER(4),
    name VARCHAR2(30)
);

CREATE SEQUENCE seq1
START WITH 1
INCREMENT BY 1
MINVALUE 1
MAXVALUE 10;

INSERT INTO tb1 VALUES (seq1.nextval, 'aa');
INSERT INTO tb1 VALUES (seq1.nextval, 'ee');
INSERT INTO tb1 VALUES (seq1.nextval, 'rr');
INSERT INTO tb1 VALUES (seq1.nextval, 'yy');
```