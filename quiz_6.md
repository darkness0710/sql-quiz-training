https://sqliteonline.com/

```
CREATE TABLE process_logs
(
Workflow    VARCHAR(100),
LogMessage  VARCHAR(100),
Occurrences INTEGER,
PRIMARY KEY (Workflow, LogMessage)
);

INSERT INTO process_logs VALUES
('Alpha','Error: Conversion Failed',5),
('Alpha','Status Complete',8),
('Alpha','Error: Unidentified error occurred',9),
('Bravo','Error: Cannot Divide by 0',3),
('Bravo','Error: Unidentified error occurred',1),
('Charlie','Error: Unidentified error occurred',10),
('Charlie','Error: Conversion Failed',7),
('Charlie','Status Complete',6);
```

Viết sql để lấy ra giá trị max Occurrences của mỗi Workflow theo thứ tự Workflow tăng dần.

|Workflow | LogMessage                              | Occurrences
| :---:   | :---:                                   | :---: 
| Alpha   | Error: Unidentified error occurred      | 9
| Bravo   | Error: Cannot Divide by 0               | 3
| Charlie | Error: Unidentified error occurred      | 10
