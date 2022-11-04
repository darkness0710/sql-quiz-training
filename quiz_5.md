```
CREATE TABLE medias (id INTEGER, ids VARCHAR(100));
INSERT INTO medias VALUES(1, '[1,2,3]');

CREATE TABLE forms (id INTEGER, media_id INTEGER);
INSERT INTO forms VALUES(1,1), (2,2), (3,5);
```
Thực hiện truy vấn sql để lấy toàn bộ bản ghi ở bảng forms với điều kiện là toàn bộ giá trị ids ở bảng medias

Answers:
```
With tmp AS (
    SELECT REPLACE(REPLACE(ids, '[', ''), ']', '') as x FROM medias
)
SELECT forms.id from forms where FIND_IN_SET (forms.media_id, (select tmp.x FROM tmp))
```
