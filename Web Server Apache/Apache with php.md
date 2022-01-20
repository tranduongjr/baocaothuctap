# 1. Cài đặt apache

Như đã cài trước đó

# 2. Cài PHP

Thêm Remi repo:

- rpm -Uvh http://rpms.remirepo.net/enterprise/remi-release-7.rpm

<img src="img/12.png">

Cài yum-untils để lấy tiện ích yum-config-manager:

<img src="img/13.png">

Cập nhật:

<img src="img/14.png">

Cài đặt PHP 7.0

- yum-config-manager --enable remi-php70
- yum -y install php php-opcache

<img src="img/15.png">

<img src="img/16.png">

Khởi động lại Apache

Sau đó tạo file index.php trong /var/www/html/tranduongjr.com và push nội dung vào.

<img src="img/18.png">

<img src="img/17.png">

