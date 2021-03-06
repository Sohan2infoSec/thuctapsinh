# Mục lục 
[I. Khái niệm](#a)

<a name="a">

# I.Một số khái niệm </a>

# 1. Cơ sở dữ liệu
Là tập hợp các dữ liệu có cấu trúc được lưu trữ trên các thiết bị lưu trữ nhằm phục vụ cho nhiêu mục của một cá nhân hay một tổ chức nào đó

# 2. Hệ quản trị cơ sở dữ liệu(DBMS)
Một hệ thống quản lý cơ sở dữ liệu lưu trữ dữ liệu theo cách mà việc truy xuất, thao tác và sản xuất thông tin trở nên dễ dàng hơn.

Hệ quản trị cơ sở dữ liệu (Database Management System-DBMS) là một hệ thống được thiết kế dùng để quản trị một cơ sở dữ liệu. Trên đó người dùng có thể định nghĩa, thao tác, và xử lí dữ liệu trong một hệ quản trị CSDL. Hầu hết hệ quản trị cơ sở dữ liệu đều thực hiện các chức năng sau:
* Lưu trữ dữ liệu.
* Tạo và duy trì cấu trúc dữ liệu.
* Hỗ trợ bảo mật.
* Cho xem và xử lý các dữ liệu lưu trữ.
* Cung cấp một cơ chế chỉ mục hiệu quả để truy cập nhanh các dữ liệu lụa chọn.
* Cung cấp tính nhất quán giữa các bản ghi khác nhau.
* Bảo vệ dữ liệu khỏi mất mát bằng các quá trình sao lưu (backup) và phục hồi (recovery).
## Kiến trúc của DBMS 

![](https://github.com/duckmak14/thuctapsinh/blob/master/Anhduc/DBMS-SQL/images/screenshot.png)

Kiến trúc của DBMS gồm 3 tầng
- Tầng cơ sở dữ liệu: Ở tầng này, cơ sở dữ liệu nằm cùng với các ngôn ngữ xử lý truy vấn của nó
- Tầng ứng dụng: Ở tầng này nằm trong máy chủ ứng dụng và các chương trình truy cập cơ sở dữ liệu. Đối với người dùng, tầng ứng dụng này trình bày một cái nhìn trừu tượng về cơ sở dữ liệu. Người dùng cuối không biết về bất kỳ sự tồn tại của cơ sở dữ liệu ngoài ứng dụng
- Tầng người dùng: Người dùng cuối hoạt động trên tầng này và họ không biết gì về bất kỳ sự tồn tại nào của cơ sở dữ liệu ngoài lớp này.

## Phân loại DBMS 
DBMS được phân loại theo cấu trúc và mô hình dữ liệu.
- Mô hình hệ quản trị cơ sở dữ liệu quan hệ (RDBMS). Đây là mô hình phổ biết trong DBMS.

![](https://github.com/duckmak14/thuctapsinh/blob/master/Anhduc/DBMS-SQL/images/screenshot_2.png)
    - Điểm nổi bật chính của mô hình này là: 
        - Dữ liệu được lưu trữ trong các bảng được gọi là quan hệ .
        - Quan hệ có thể được bình thường hóa.
        - Trong quan hệ chuẩn hóa, các giá trị được lưu là giá trị nguyên tử.
        - Mỗi hàng trong một mối quan hệ chứa một giá trị duy nhất.
        - Mỗi cột trong một quan hệ chứa các giá trị từ cùng một miền.
- Mô hình quản trị cơ sở dữ liệu thực thể (ER)

![](https://github.com/duckmak14/thuctapsinh/blob/master/Anhduc/DBMS-SQL/images/screenshot_1.png)
    - Mô hình ER xác định khung nhìn khái niệm của cơ sở dữ liệu. Nó hoạt động xung quanh các thực thể

# 3. Bảng 
Bảng là một đối tượng được sử dụng để tổ chức và lưu trữ dữ liệu. Một cơ sở dữ liệu bao gồm nhiều bảng. Các bảng đều có mối liên hệ với nhau.

## Mối quan hệ giữa các bảng
`Quan hệ 1-1` :  là quan hệ mà một bản ghi của bảng A quan hệ với duy nhất với một bản ghi của bảng B và ngược lại

`Quan hệ 1-n` là quan hệ một bản ghi của bảng A quan hệ với nhiều bản ghi của bảng B

`Quan hệ n-n` là quan hệ nhiều bản ghi của bảng A quan hệ với nhiều bản ghi của bảng B.
# 4. Khóa 
## khóa chính
Khóa chính là để định danh duy nhất mỗi bản ghi trong một bảng của cơ sở dữ liệu.

Dữ liệu trong trường khóa chính phải là duy nhất và không được chứa giá trị NULL Một trường với một giá trị NULL là một trường không có giá trị (Trường có giá trị NULL là giá trị đã để trống trong quá trình tạo bản ghi)

Mỗi bảng chỉ có một khóa chính và khóa chính có thể tạo ra từ nhiều trường trong bảng.

## Khóa ngoại
Khóa ngoại của bảng này được coi như một con trỏ trỏ tới khóa chính của bảng khác.

Hay có thể hiểu một trong bảng này có một trường mà trường này lại là khóa chính của một bảng khác. Thì trường đó trong bảng này được gọi là khóa ngoại.

# 5. Dạng chuẩn của CSDL
Chuẩn hóa là quá trình phân tách các bảng thành các bảng nhỏ hơn dựa và các phụ thuộc hàm

Các dạng chuẩn là các chỉ dẫn để thiết kế các bảng trong CSDL.

Mục đích của chuẩn hóa là làm giảm dữ liệu dư thừa và các lỗi xảy ra khi cập nhật CSDL. Nhưng điều này làm tăng thời gian truy vấn dữ liệu.

## 5.1 Dạng chuẩn 1NF: Không có phần tử/nhóm phần tử lặp
Một bảng được gọi là 1NF: 
- khi và chỉ khi toàn bộ các miền giá trị của các cột có mặt trong bảng đều chỉ chứa các giá trị nguyên tử (nguyên tố) không được có giá trị NULL 
- Mỗi hàng phải có một thuộc tính nhận dạng duy nhất (Khóa chính)
## 5.2 Dạng chuẩn 2NF
Mối quan hệ ở dạng chuẩn 2NF nếu:
- Là 1NF
- Các thuộc tính không khóa phụ thuộc hàm không đầy đủ vào khóa chính.

Một quan hệ ở dạng chuẩn 2NF nếu thỏa mãn 1 trong các điều kiện sau:
- Khóa chính chỉ gồm một thuộc tính
- Bảng không có các thuộc tính không khóa
- Tất cả các thuộc tính không khóa phụ thuộc hoàn toàn vào các thuộc tính khóa chính.

## 5.3 Dạng chuẩn 3NF 
Một quan hệ ở dạng chuẩn 3NF nếu quan hệ đó:
- Là 2NF
- Các thuộc tính không khóa phải phụ thuộc trực tiếp vào khóa chính

# 6. SQL
SQL viết tắt của Structured Query Language (ngôn ngữ truy vấn cấu trúc). công cụ sử dụng để tổ chức, quản lý và truy xuất dữ liệu đuợc lưu trữ trong các cơ sở dữ liệu. SQL là một hệ thống ngôn ngữ bao gồm tập các câu lệnh sử dụng để tương tác với cơ sở dữ liệu quan hệ.

SQL không chỉ dùng để truy xuất dữ liệu mà SQL được sử dụng để điều khiển tất cả các chức năng mà một hệ quản trị cơ sở dữ liệu cung cấp cho người dùng bao gồm:
- Có thể truy vấn Database theo nhiều cách khác nhau, bởi sử dụng các lệnh.
- Người dùng có thể truy cập dữ liệu từ RDBMS.
- SQL cho phép người dùng miêu tả dữ liệu.
- SQL cho phép người dùng định nghĩa dữ liệu trong một Database và thao tác nó khi cần thiết.
- Cho phép người dùng tạo, xóa Database và bảng.
- Cho phép người dùng tạo view, Procedure, hàm trong một Database.
- Cho phép người dùng thiết lập quyền truy cập vào bảng, thủ tục và view.


