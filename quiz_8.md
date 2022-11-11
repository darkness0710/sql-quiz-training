https://sqliteonline.com/
```
CREATE TABLE persons
(
    spaceman_id      INTEGER PRIMARY KEY,
    job_description  VARCHAR(100),
    mission_count    INTEGER
);

INSERT INTO persons VALUES
(1001,'Astrogator',6),(2002,'Astrogator',12),(3003,'Astrogator',17),
(4004,'Geologist',21),(5005,'Geologist',9),(6006,'Geologist',8),
(7007,'Technician',13),(8008,'Technician',2),(9009,'Technician',7);
```

Viết sql để để hiển thị như bảng sau!

|Job Description | Most Experienced                              | Least Experienced
| :---:   | :---:                                   | :---: 
| Astrogator   | 3003      | 1001
| Geologist   | 4004               | 6006
| Technician | 7007      | 8008
