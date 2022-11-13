https://sqliteonline.com/
```
CREATE TABLE log_shoppings (
    id integer primary key,
    user_id INT,
    created_at DATE 
);

INSERT INTO log_shoppings VALUES (1, 1, '2022-11-01');
INSERT INTO log_shoppings VALUES (2, 2, '2022-11-01');
INSERT INTO log_shoppings VALUES (3, 3, '2022-11-01');
INSERT INTO log_shoppings VALUES (4, 1, '2022-11-02');
INSERT INTO log_shoppings VALUES (5, 2, '2022-11-02');
INSERT INTO log_shoppings VALUES (6, 1, '2022-11-03');
INSERT INTO log_shoppings VALUES (7, 3, '2022-11-03');
INSERT INTO log_shoppings VALUES (8, 1, '2022-11-04');
INSERT INTO log_shoppings VALUES (9, 1, '2022-11-06');
INSERT INTO log_shoppings VALUES (10, 1, '2022-11-07');
INSERT INTO log_shoppings VALUES (11, 1, '2022-12-07');
INSERT INTO log_shoppings VALUES (12, 1, '2022-12-08');
```
In ra câu sql để đếm số ngày liên tiếp lớn nhất của mỗi user khi mua hàng!

| user_id  | max 
| ----     | ----
| 1        |   4
| 2        |  2
| 3        |   1
