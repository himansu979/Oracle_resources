# SQL
- Oracle Live SQL : https://livesql.oracle.com/apex/f?p=590:1000
- PL/SQL tutorial (guru99) : https://www.guru99.com/pl-sql-tutorials.html
- PL/SQL tutorialspoint : https://www.tutorialspoint.com/plsql/index.htm
- PL/SQL tutorial : https://www.oracletutorial.com/plsql-tutorial/
- Tech on the Net : https://www.techonthenet.com/oracle/index.php

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
