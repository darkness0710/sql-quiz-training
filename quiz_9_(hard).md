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
![image](https://user-images.githubusercontent.com/25264763/201518914-0a7c1f8c-a96c-4481-af97-ca7a716ddde9.png)

In ra câu sql để đếm chuỗi ngày mua hàng liên tục nhiều nhất của mỗi user!

| user_id  | max 
| ----     | ----
| 1        |   4
| 2        |  2
| 3        |   1
