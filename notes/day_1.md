## Database là gì?
- Theo wikipedia, cơ sở dữ liệu (Database) là một tập hợp các dữ liệu có tổ chức liên quan đến nhau, thường được lưu trữ và truy cập điện tử từ hệ thống máy tính. Khi cơ sở dữ liệu phức tạp hơn, chúng thường được phát triển bằng cách sử dụng các kỹ thuật thiết kế và mô hình hóa chính thức.

## SQL là gì?
- SQL là viết tắt của Structured Query Language, là ngôn ngữ truy vấn có cấu trúc, cho phép bạn truy cập và thao tác với các cơ sở dữ liệu để tạo, xóa, sửa đổi, trích xuất dữ liệu. Các hệ thống quản trị cơ sở dữ liệu như MySql, MS Access, Oracle, Sybase, Informix, Postgres hay SQL Server đều lấy SQL làm ngôn ngữ cơ sở dữ liệu tiêu chuẩn. Càng về sau này thì các ứng dụng đòi hỏi phải có tốc độ xử lý dữ liệu ngày càng nhanh, dẫn đến sự nổi lên của NoSQL(cơ sở dữ liệu phi quan hệ): MapReduce và Bigtable, Cassandra, MongoDB, và nhiều nữa.

## Table
- Một bảng nó lưu trữ và hiện thị thông tin với cấu trúc gồm có các cột và các hàng.
Cơ sở dữ liệu sẽ có nhiều bảng, mỗi bảng được thiết kế với mục đích lưu trữ một loại thông tin nhất định.

Ví dụ bảng users lưu thông tin người dùng như sau:
id | name | email | created_at | updated_at | deleted_at
--- | --- | --- | --- |--- |--- 
1   | abc | abc@gmail.com | 2012-12-12 09:00 | 2012-12-12 09:00 | NULL
2   | xyz | xyz@gmail.com | 2012-12-12 09:00 | 2012-12-12 09:00 | NULL

# Primary Key
Trong bảng, trường cột được đặt là khóa chính primary key thì trường đó là duy nhất cho từng dữ liệu theo dòng (mỗi dòng gọi là một record).

Khóa chính Primary Key có các đặc tính sau:
- Là duy nhất cho mỗi cột, dòng khác nhau thì giá trị này khác nhau
- Không được nhận giá trị rỗng NULL
- Mỗi bảng sẽ có tối đa 1 khóa chính (Ngoài ra khóa chính có thể được tạo ra từ tổ hợp 1 cột hoặc nhiều cột)

# Foreign Key
- Khóa ngoại của một table được xem như con trỏ trỏ tới khóa chính của table khác.
- Một table có thể có nhiều khóa ngoại.
- Để dễ hiểu ta có ví dụ sau, giả sử có 2 bảng users và bảng logs:

```Bảng users```
id | name | email | created_at | updated_at | deleted_at
--- | --- | --- | --- |--- |--- 
1   | abc | abc@gmail.com | 2012-12-12 09:00 | 2012-12-12 09:00 | NULL
2   | xyz | xyz@gmail.com | 2012-12-12 09:00 | 2012-12-12 09:00 | NULL

```Bảng logs```
id | user_id | note
--- | --- | --- 
1   | 1 | Login with IP 1.2.3.4
2   | 2 | Login with IP 5.6.7.8

Ở bảng logs thì id là khóa chính còn user_id là khóa ngoại. (khóa ngoại của bảng này sẽ là khóa chính của 1 bảng khác)
