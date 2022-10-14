#tables x_items
| name
| :---:
| item_1
| item_2
| item_3

#tables y_items
| name
| :---:
| item_1
| item_2
| item_4

https://sqliteonline.com/
```
CREATE TABLE 'x_items'
(name VARCHAR(100) PRIMARY KEY);


CREATE TABLE 'y_items'
(name VARCHAR(100) PRIMARY KEY);

INSERT INTO x_items (name) VALUES ('item_1'),('item_2'),('item_3');
INSERT INTO y_items (name) VALUES ('item_1'),('item_2'),('item_4');
```

#Write an SQL statement to transform the following tables into the expected output.
| x_name | y_name
| :---:  | :---:
| item_1 | item_1
| item_2 | item_2
| item_3 | NULL
| NULL   | item_4

Answer:
```
SELECT x_items.name as x_name, y_items.name as y_name
FROM x_items FULL JOIN y_items on x_items.name = y_items.name;
```
