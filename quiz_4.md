```
CREATE TABLE users (user_id INTEGER);
CREATE TABLE user_followers (parent_id INTEGER, user_sub_id INTEGER);
CREATE TABLE jobs (user_id INTEGER,job_id INTEGER);

INSERT INTO users VALUES (1), (2), (3), (4), (5);
INSERT INTO user_followers VALUES (1,2), (1,3), (1,4), (2,3), (2,5);
INSERT INTO jobs VALUES (1,1), (2,2), (4,3), (5,4), (1,5);
```


table: users
| user_id
| :---: 
| 1
| 3
| 4
| 5


table: user_followers
| parent_id    | user_sub_id
| :---:        |    :---:   
| 1            | 2
| 1            | 3
| 1            | 4
| 1            | 3
| 2            | 5



Viết sql trả về kết quả sau (Trả về job_ids mà user_id đó sở hữu (bao gồm cả các job_id của sub_id))
| user_id_unique    | job_ids_value      
| :---:             | :---:             
| 1                 | 1,2,5,3
| 2                 | 2,4
| 3                 | Null
| 4                 | 3
| 5                 | 4

