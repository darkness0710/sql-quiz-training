https://sqliteonline.com/
```
CREATE TABLE PhoneDirectories
(
CustomerID  INTEGER,
[Type]      VARCHAR(100),
PhoneNumber VARCHAR(12),
PRIMARY KEY (CustomerID, [Type]));

INSERT INTO PhoneDirectories VALUES
(1001,'Cellular','555-897-5421'),
(1001,'Work','555-897-6542'),
(1001,'Home','555-698-9874'),
(2002,'Cellular','555-963-6544'),
(2002,'Work','555-812-9856'),
(3003,'Cellular','555-987-6541');
```
Question: Write sql show result

| CustomerID    | Cellular           | Work              | Home
| :---:         | :---:              | :---:             | :---:       
| 1001          | 555 - 897 - 5421   | 555 - 897 - 6542  | 555 - 698 - 9874
| 2002          | 555 - 897 - 6544   | 555 - 812 - 9856  | NULL
| 3003          | 555 - 897 - 6541   | NULL              | NULL

Answer example:
```
With TableA AS (SELECT customerid, phonenumber as Cellular
		FROM PhoneDirectories
		WHERE type = 'Cellular'),
	TableB AS (SELECT customerid, phonenumber as Work
		FROM PhoneDirectories
		WHERE type = 'Work'),
	TableC AS (SELECT customerid, phonenumber as Home
		FROM PhoneDirectories
		WHERE type = 'Home')
SELECT TableA.customerid, Cellular, Work, Home 
FROM TableA
FULL JOIN TableB on TableA.customerid = TableB.customerid
FULL JOIN TableC on TableA.customerid = TableC.customerid;
```
