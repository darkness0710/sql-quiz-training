https://sqliteonline.com/
```
CREATE TABLE sales
(
[Year]  INTEGER,
Amount  INTEGER
);

INSERT INTO sales VALUES (2017, 100), (2017, 200), (2018, 300), (2019, 500);
```
Viết sql tính sum mỗi năm và hiển thị theo dạng cột.

|2017   | 2018  | 2019
| :---: | :---: | :---:
|300    | 300   | 500   

Answer example:
```
SELECT SUM(CASE WHEN ( YEAR = '2017' ) then Amount else '' end) as '2017',
       SUM(CASE WHEN ( YEAR = '2018' ) then Amount else '' end) as '2018',
       SUM(CASE WHEN ( YEAR = '2019' ) then Amount else '' end) as '2019'
from sales
 ```
