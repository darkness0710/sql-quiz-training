https://sqliteonline.com/
```
CREATE TABLE logs
(
user_id  INTEGER,
point  INTEGER,
created_at TIMESTAMP
);

INSERT INTO logs VALUES
    (1, 100, '2012-01-01'),
    (1, 200, '2012-01-02'),
    (1, -1, '2012-01-03'),
    (1, 300, '2012-01-04'),
    (1, 400, '2012-01-05'), 
    (2, 100, '2012-01-06'), 
    (1, 500, '2012-01-07'), 
    (1, -2, '2012-01-08'), 
    (1,111, '2012-01-09'), 
    (1, 211, '2012-01-10'), 
    (1, 311, '2012-01-11');
```
Viết sql tìm chuỗi tiền dương liên tục dài nhất của mỗi user và in ra value tổng lớn nhất của chuỗi đó  (Trường hợp 2 chuỗi dài bằng nhau, lấy chuỗi có tổng lớn hơn)
```
user_id     | maxium_step  | value
1              3             1200
2              1             100
```
