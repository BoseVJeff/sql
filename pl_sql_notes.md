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