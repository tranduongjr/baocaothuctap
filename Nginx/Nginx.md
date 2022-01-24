# Cài đặt Nginx

1. Update và cài thêm epel

```
yum update

yum install epel-release -y
```

2. Cài Nginx

<img src="img/1.png">

3. Tạo thư mục chứa Vhost

```
mkdir -p /var/www/html/tranduongjr.com

mkdir -p /var/www/html/tranduongjr.com/logs
```

Phân quyền

```
chown -R nginx:nginx /var/www/html/tranduongjr.com

Tạo File index.html

```
vi /var/www/html/tranduongjr.com/index.html


<img src="img/2.png">

<img src="img/3.png">

4. Tạo Vhost

Tất cả các file Vhost của nginx nằm tại  thư mục /etc/nginx/conf.d . Để tiện tquarn lý mỗi website thì ta nên có 1 vhost riêng. 

Ở đây vhost tranduongjr.com sẽ được đặt tại file tranduongjr.com.conf

```
vi /etc/nginx/conf.d/tranduongjr.com.conf
```

Cấu hình file Vhost

<img src="img/5.png">

Khởi động nginx
```
systemctl start nginx
```

<img src="img/6.png">

2. Cài PHP 

Tương tự như cài đối với apache

Thêm remi repo

```
rpm -Uvh http://rpms.remirepo.net/enterprise/remi-release-7.rpm
```

Cài Yum-utils để lấy tiện ích yum-config-manager:

```
yum -y install yum-utils
```

Cài PHP 7.0

```
yum-config-manager --enable remi-php70

yum -y install php php-opcache
```



