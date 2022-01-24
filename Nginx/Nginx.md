# Cài đặt Nginx

1. Update và cài thêm epel

```
yum update

yum install epel-release -y
```


2. Cài Nginx

```
yum install nginx
```

<img src="img/1.png">

Sau đó khởi động nginx

```
systemctl enable nginx

systemctl start nginx
```

<img src="img/3.png">

Kiểm tra hoạt động của nginx (nhập địa chỉ ip của webserver)

<img src="img/2.png">

## Cài PHP

Cài 2 gói php-mysql và php-fpm

```
yum install php php-mysql php-fpm
```

<img src="img/4.png">

Sau đó cấu hình các thông số cho PHP. Ta mở file cấu hình php-fpm với dòng lệnh:

```
vi /etc/php.ini
```

Tìm đến tham số cgi.fix_pathinfo đang được comment lại bằng dấu ; và thiết lập giá trị cho tham số này bằng 0. Đây là một thiết lập cực lỏng lẻo về bảo mật, tham số này cho phép PHP sẽ thực thi một file gần nó nhất nếu không có file PHP nào phù hợp. Sử dụng /<từ tìm kiếm> để tìm kiếm trong vi

Chuyển tham số cgi.fix_pathinfo=0 chuyển thành 1

<img src="img/5.png">

Lưu lại và thoát

Tiếp đến mở file cấu hình php-fpm.d/www/conf

```
vi /etc/php-fpm.d/www/conf
```

Tìm đến tham số listen và thay bằng:

<img src="img/6.png">

Tìm đến listen.owner và listen group rồi bỏ comment(;) đi

<img src="img/7.png">

Tìm đến tham số user = apache, group = apache và thay bằng nginx:

<img src="img/8.png">

Như vậy ta đã cấu hình xong file www.conf thực hiện lưu và thoát sau đó khởi động php-fpm.

```
systemctl enable php-fpm

systemctl start php-fpm
```

<img src="img/9.png">

**Cấu hình nginx để xử lý các trang PHP**

