https://sqliteonline.com/

```
CREATE TABLE orders
(
CustomerID      INTEGER,
OrderID         VARCHAR(100),
DeliveryState   VARCHAR(100),
Amount          MONEY,
PRIMARY KEY (CustomerID, OrderID)
);


INSERT INTO orders
VALUES
(1001,'Ord936254','CA',340),(1001,'Ord143876','TX',950),(1001,'Ord654876','TX',670),
(1001,'Ord814356','TX',860),(2002,'Ord342176','WA',320),(3003,'Ord265789','CA',650),
(3003,'Ord387654','CA',830),(4004,'Ord476126','TX',120);
```
Điều kiện lọc: Hiển thị các record với điều kiện customer_id có cả DS bao gồm CA và  TX sau đó  hiển thị record chứa TX 
