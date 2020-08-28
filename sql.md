# SQL
- Oracle Live SQL : https://livesql.oracle.com/apex/f?p=590:1000
- PL/SQL tutorial (guru99) : https://www.guru99.com/pl-sql-tutorials.html
- PL/SQL tutorialspoint : https://www.tutorialspoint.com/plsql/index.htm
- Oracle tutorial PL/SQL tutorial : https://www.oracletutorial.com/plsql-tutorial/
- Tech on the Net : https://www.techonthenet.com/oracle/index.php
- PL/SQL tutorial : https://www.plsqltutorial.com/
- PL/SQL in one hour steven : https://www.youtube.com/watch?v=vR8uDZ-u0aI&feature=youtu.be
- PL-SQL tutorial : https://plsql-tutorial.com/

## CREATE OR REPLACE VIEW
https://www.techonthenet.com/oracle/views.php
```
CREATE OR REPLACE VIEW demo AS
SELECT CUST_ID, CUST_FIRST_NAME, CUST_LAST_NAME FROM SH.CUSTOMERS WHERE ROWNUM<10;

SELECT * FROM demo;

DROP VIEW demo;
```

## EXECUTE IMMEDIATE
https://www.youtube.com/watch?v=47KzYVBNbIs
```
DECLARE
sql_query VARCHAR2(150);
tot_count NUMBER(6);

BEGIN
sql_query := 'SELECT COUNT(*) FROM SH.CUSTOMERS';
DBMS_OUTPUT.PUT_LINE(sql_query);
EXECUTE IMMEDIATE sql_query INTO tot_count;
DBMS_OUTPUT.PUT_LINE('Total count is : ' || tot_count);
END;
/
```

## CREATE OR REPLACE PROCEDURE
https://www.guru99.com/subprograms-procedures-functions-pl-sql.html
```
CREATE OR REPLACE PROCEDURE welcome_msg (p_name IN VARCHAR2) 
IS
BEGIN
dbms_output.put_line ('Welcome '|| p_name);
END;
/

EXEC welcome_msg ('Guru99');
```

## CREATE OR REPLACE FUNCTION
```
CREATE OR REPLACE FUNCTION welcome_msg_func ( p_name IN VARCHAR2) RETURN VARCHAR2
IS
BEGIN
RETURN ('Welcome ' || p_name);
END;
/

SELECT welcome_msg_func('Guru99') FROM DUAL;

DECLARE
lv_msg VARCHAR2(250);
BEGIN
lv_msg := welcome_msg_func ('Himansu');
dbms_output.put_line(welcome_msg_func('Guru99'));
dbms_output.put_line(lv_msg);
END;
/
```





