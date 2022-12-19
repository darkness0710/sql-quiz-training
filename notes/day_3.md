## Insert dữ liệu vào table
Cú pháp đầy đủ:
```
INSERT INTO your_table (column_name1, column_name2, ...) VALUES ('value_1', 'value_2');
```

Cú pháp rút gọn:
```
INSERT INTO your_table VALUES ('value_1', 'value_2'); // Map dựa vào thứ tự cột trong table
```
## Câu lệnh SELECT
Cú pháp cơ bản câu lệnh SELECT trong sql trong trường hợp chỉ muốn lấy ra một số cột trong table:
```
SELECT column1, column2, columnN FROM table_name;
```
Ngoài ra nếu muốn hiển thị toàn bộ các cột trong bảng có thể sử dụng biểu thức *, ví dụ:
```
SELECT * FROM table_name;
```
## Mệnh đề WHERE
Cú pháp cơ bản của câu lệnh SELECT với mệnh đề WHERE:
```
SELECT column1, column2, columnN 
FROM table_name
WHERE [condition]
```

## Ví dụ
1. Chúng ta tạo một bảng users như sau:
```
CREATE TABLE users
( 
    id NUMBER PRIMARY KEY,
    username varchar(25) NOT NULL,
    email varchar(30) NOT NULL,
    age INT
);
```
2. Insert dữ liệu vào bảng
```
INSERT INTO users (id, username, email, age) VALUES ('1', 'xxx', 'xxx@gmail.com', 20);
INSERT INTO users (id, username, email, age) VALUES ('2', 'yyy', 'yyy@gmail.com', 21);
```
3. Select toàn bộ bảng users
```
SELECT * FROM users;
```
4. Tìm kiếm trong bảng users với email = 'xxx@gmail.com'
```
SELECT * FROM users WHERE email = 'xxx@gmail.com';
```
5. Tìm kiếm trong bảng user với các id > 1 và có age > 20
```
SELECT * FROM users WHERE id > 1 and age > 20;
```
