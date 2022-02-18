# Cài đặt IIS

1. Trong Server Manager => Add Roles and Features

<img src="img/1.png">

2. Để mặc định chọn Next

<img src="img/2.png">
<img src="img/3.png">
<img src="img/4.png">

Tích vào Web Server(IIS)
<img src="img/5.png">

Add Feature sau đó để các mặc định và tiếp tục chọn Next

<img src="img/6.png">

Sau khi Next hết chọn Click Install để tiến hành cài đặt

<img src="img/7.png">

Trình quản lý dịch vụ IIS trong Tools:

<img src="img/8.png">

## Tạo Web html

Các file của IIS được mặc định tại ổ C => inetpub => wwwroot. Tại đây ta sẽ tạo 1 file document text index.html và ghi nội dung đơn giản vào để tạo web HTML

<img src="img/9.png">
<img src="img/10.png">

Sửa tên file xóa đuôi .txt đi

Trỏ IP về tên miền 

<img src="img/12.png">

Kiểm tra kết quả bằng cách nhập địa chỉ IP hoặc tên miền

<img src="img/11.png">

Nếu chưa thuê tên miền hoặc trỏ bản ghi thì tại WinServer gõ 127.0.0.1 hoặc localhost:

<img src="img/13.png">

# Cài đặt Wordpress

1. Dowload PHP theo link: https://windows.php.net/download/

2. Dowload PHP Manager theo link: https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10 và tiến hành cài đặt

3. Giải nén PHP vừa tạo vào đường dẫn : C:\PHP\

## Cài đặt SQL Server

Tải MySQL Community Server theo link: https://dev.mysql.com/downloads/mysql/

<img src="img/20.png">

Cài đặt

Chọn Server Only và Next

<img src="img/21.png">

Chọn Excute và Next

<img src="img/22.png">

Chọn Server Computer và Port để mặc định là 3306

<img src="img/23.png">

Thêm Password cho MySQL root và tạo User quản trị DB sau đó nhấn Next

<img src="img/24.png">

Chọn Excute

<img src="img/25.png">

Finish

## Cài phpMyAdmin để quản lý MySQL
Tải phpmyadmin theo link : https://www.phpmyadmin.net/ và giải nén vào 1 folder C:\internalWeb\phpMyAdmin

<img src="img/27.png">

Phân thêm quyền Modify cho người dùng IUSR và IIS_IUSR cho thư mục internalWeb

<img src="img/28.png">

Vào IIS Manager vào tùy chọn Site => Add Website và điền các thông tin tương ứng

<img src="img/29.png">

<img src="img/30.png">

Vào tùy chọn PHP Manager để tiến hành cài đặt PHP cho Site

<img src="img/31.png">

Register new PHP version

<img src="img/32.png">

Trỏ đến file php-cgi.exe đã giải nén trong C:\PHP để cài đặt

<img src="img/33.png">

Kết quả đã cài PHP 7.3.33 thành công cho Site

<img src="img/34.png">

Truy cập vào tranduongjr.com/phpmyadmin để vào trang quản trị phpmyadmin và đăng nhập với User password DBadmin đã tạo ở MySQL

<img src="img/35.png">

Tạo cơ sở dữ liệu cho Wordpress vào chọn ``` Mới ``` và đặt tên cho cơ sở dữ liệu

<img src="img/36.png">

Cơ sở dữ liệu mới được tạo:

<img src="img/37.png">

**WordPress**

Tải xuống WordPress theo link: https://vi.wordpress.org/download/

<img src="img/38.png">

Chúng ta được khuyến cáo không nên sử dụng thư mục inetpub (do IIS cũng cấp) cho các trang web của mình vì kể từ Server 2003 khi nó là một lỗ hổng và tất cả các cuộc tấn công thường nhắm vào thư mục đó.

Tạo một thư mục trong thư mục gốc C có tên wordpress và giải nén tệp cài đặt wordpress ở đó. Người dùng IUSR có quyền đối với nó (tương tự như với thư mục phpMyAdmin ở trên)

<img src="img/39.png">

Trước khi tạo một web mới trong IIS, ta mở IIS Manager và thêm một Application Pools mới cho wordpress

<img src="img/40.png">

Ta nên xóa trang web mặc định để điều hướng đến site wordpress

<img src="img/41.png">

Tiếp đến ta tạo web mới cho wordpress

Tại Sites chọn chuột phải Add Websites

<img src="img/42.png">

Lưu ý: do trên ta tạo Sites internalWeb cho trang quản trị phpMyAdmin dùng port 80 nên nếu muốn dùng port 80 cho wordpress ta cần đổi port internalWeb sang port khác trong mục binldings

<img src="img/43.png">

Kiểm tra trong PHP Manager xem site wordpress đã được kích hoạt PHP chưa nếu chưa thì kích hoạt (tương tự như với internalWeb ở trên)

Tạo tài khoản trong phpMyAdmin:
<img src="img/45.png">

Truy cập vào trang quản trị WP và tiến hành cài đặt

<img src="img/44.png">

<img src="img/46.png">

Đăng nhập với tài khoản đã cài đặt

<img src="img/47.png">

Trang quản trị WP hiện ra

<img src="img/48.png">

Như vậy ta đã hoàn tất quá trình cài đặt website chạy wordpress với IIS và sql server
