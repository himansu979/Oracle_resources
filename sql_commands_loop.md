
## Loop

```
DECLARE 
a NUMBER:=1; 
BEGIN
dbms_output.put_line('Program started.');
LOOP
dbms_output.put_line(a);
a:=a+1;
EXIT WHEN a>5;
END LOOP;
dbms_output.put_line('Program completed');
END;
/
```
## outer_loop, inner_loop

```
DECLARE
a NUMBER:=0;
b NUMBER;
upper_limit NUMBER :=4;
BEGIN
dbms_output.put_line('Program started.' );
<<outer_loop>>
LOOP 
a:=a+1;
b:=1;
<<inner_loop>>
LOOP
EXIT outer_loop WHEN a > upper_limit;
dbms_output.put_line(a);
b:=b+1;
EXIT inner_loop WHEN b>a;
END LOOP;
END LOOP;
dbms_output.put_line('Program completed.');
END;
/
```

## Foor loop

```
BEGIN
dbms_output.put_line('Program started.' );
FOR a IN 1 .. 5
LOOP
dbms_output.put_line(a);
END LOOP;
dbms_output.put_line('Program completed.'); 
END;
/
```

## Nested Foor loop

```
DECLARE
b NUMBER;
BEGIN
dbms_output.put_line('Program started' );
FOR a IN 1 .. 3
LOOP
b:=1;
WHILE (a>=b)
LOOP
dbms_output.put_line(a);
b:=b+1;
END LOOP;
END LOOP;
dbms_output.put_line('Program completed' );
END;
/
```

## while loop

```
DECLARE
a NUMBER :=1;
BEGIN
dbms_output.put_line('Program started');
WHILE (a <= 5) 
LOOP
dbms_output.put_line(a);
a:=a+1;
END LOOP;
dbms_output.put_line('Program completed' ); 	
END;
/
```






