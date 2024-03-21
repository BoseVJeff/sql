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