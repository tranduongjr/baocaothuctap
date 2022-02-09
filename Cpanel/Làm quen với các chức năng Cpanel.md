# Các chức năng trên WHM (Web Host Manager)

WHM được truy cập ở port 2087

Các chức năng chính của WHM:

<img src="img/24.png">

1. Server Configuration: Cấu hình liên quan tới Server

- Quản lý cài đặt Web
- Thay đổi Password Root
- Configure CPanel Analytics
- Cấu hình các Cron jobs Cpanel
- Initial Quota Setup
- Link Server Nodes
- Quản lý Profile Server
- Thông tin thời gian trên Server
- Thống kê cấu hình các phần mềm
- Cửa sổ Terminal
- Chỉnh sửa các cài đặt
- Cập nhật các tiện ích
- WHM Marketplace

2. Support: Khởi tạo các Ticket và hộ trợ kiểm soát truy cập Cpanel

3. Networking Setup: Chỉnh sửa hostname và DNS

4. Security Center: Các bảo mật nâng cao

5. Server Contact: Thiết lập các cảnh báo từ Server tới mail quản trị

6. Reseller

- Thay đổi quyền sở hữu của một Account nào đó
- Thay đổi quyền sở hữu của nhóm Account nào đó
- Chỉnh sửa servername của reseller và các đặc quyền tương ứng
- Gửi cảnh báo tới các Reseller
- Quản lý ủy quyền các IP của Reseller
- Quản lý chia sẻ IP của Reseller
- Trung tâm quản lý Reseller
- Hiển thị các Reseller Account
- Xem trạng thái của các Reseller Account

7. Service Configuration: Cấu hình dịch vụ

8. Locales: Cấu hình thay đổi ngôn ngữ.

9. Backup: Backup hoặc Restore dữ liệu

10. Clusters

11. System Reboot: Khởi động lại hệ thống

12. Server Status: Xem trạng thái của hệ thống, các dịch đang chạy,...

13. Account Information: Thông tin các tài khoản

- Danh sách các tài khoản
- Danh sách các Domain
- Danh sách các Subdomain
- Danh sách các tài khoản đã bị tạm ngưng
- Hiển thị các tài khoản vượt quá giới hạn
- Xem băng thông sử dụng

14. Account Functions: Nơi thực thi các thiết lập với tài khoản

- Thay đổi địa chỉ của Site
- Tạo tài khoản mới
- Gửi cảnh báo tới tất cả các User
- Thay đổi password của Account
- Giới hạn băng thông sử dụng cho các Account
- Quản lý đình chỉ các Account
- Quản lý chế độ demo cho Account
- Sửa đổi mật khẩu
- Sửa đổi giới hạn Account
Và các tính năng khác như Reset băng thông, xóa Account, giải phóng băng thông,...

15. Tranfers: Truyền dữ liệu

- Chuyển dữ liệu từ Addon Domain tới Account
- Xem lại quá trình chuyển và khôi phục dữ liệu
- Chuyển và khôi phục một Account Cpanel
- Tranfer tool

16. Themes: Thay đổi giao diện của WHM

17. Packages: Quản lý các Package

- Tạo Packages
- Xóa Packages
- Chỉnh sửa Packages
- Feature Manager

18. DNS Function: Các tính năng quản lý DNS

- Thêm 1 DNS Zone
- Xóa 1 DNS Zone
- Quản lý các DNS Zone
- Chỉnh sửa Zone Templates
- Chỉnh sửa cấu hình các bản ghi mail
- Chỉnh sửa Nameserver

19. SQL Services: Quản lý dịch vụ SQL

Quản lý các Database, Username, Password, phpmyadmin, các tiến trình MySQL,...

20. IP Functions: Các tính năng liên quan tới quản lý các IP

21. Software

- EasyApache
- Cài đặt các Modules 
- Quản lý MultiPHP
- Quản lý Nginx
- Cập nhật hệ thống
- Cập nhật các phần mềm

22. Email: Quản lý các cấu hình liên quan tới Mail

23. System Health: Quản lý các tiến trình, trạng thái của hệ thống

24. CPanel: Quản lý các cầu hình, log, các Plugin hay các cài đặt cho Cpanel

25. SSL/TLS: Quản lý SSL Certificate cho các domain 

26. Market

27. Restart Services: Khởi động lại các dịch vụ của hệ thống như DNS Server, HTTP Server (Apache), IMAP,...

28. Development: Các tính năng dành cho nhà phát triển

29. Plugins

## Tạo Package

Tại giao diện WHM ta vào tùy chọn Add a Package

<img src="img/10.png">

Sau đó điền các thông tin tùy ý cho Package và Add

<img src="img/11.png">
<img src="img/12.png">

Các tùy chọn đối với Package như thêm, xóa, sửa các package:

<img src="img/13.png">

## Tạo Account

Để tạo Account ta có thể vào Account Functions => Create a New Account hoặc tại giao diện chính cũng có tùy chọn Create a New Account

<img src="img/14.png">

Sau đó điền các thông tin để tạo account và các thiết lập đối với account sau đó nhấn Create để tạo:

<img src="img/15.png">

Thông báo trả về tạo tài khoản thành công, ta có thể truy cập vào cpanel của account này hoặc truy cập theo port 2083 và đăng nhập với thông tin đã tạo trước đó để truy cập vào trang quản trị host của account

<img src="img/16.png">

Để xem danh sách các Account hoặc chỉnh sửa thông tin, xóa account ta vào trong tùy chọn Account Information => List Account và thực thi các tùy chọn tương ứng. Tương tự cũng có các tùy chọn đối với các Subdomains, Suspended Account (các tài khoản đã bị tạm ngưng),...

<img src="img/17.png">

## Cài đặt WordPress

WordPress Toolkit là tool hỗ trợ cài WordPress tự động, trên WHM vào tùy chọn Plugins => WordPress Toolkit sau đó click vào Install

<img src="img/18.png">

Điền các thông tin khởi tạo WordPress như đường dẫn website, tiêu đề website, giao diện, ngôn ngữ, phiên bản, thông tin về tài khoản quản trị, database. Sau đó click vào Install để cài đặt.

<img src="img/19.png">

Kết quả sau khi cài đặt

<img src="img/20.png">

Có thể truy cập vào trang quản trị WordPress theo domain/wp-admin

<img src="img/23.png">

## Cài đặt SSL

Trên WHM vào tùy chọn SSL/TLS => Install an SSL Certificate on a Domain và tiến hành thêm add chứng chỉ

<img src="img/21.png">

Sau khi cài đặt thành công sẽ có thông báo trả về

<img src="img/22.png">

# Các chức năng trên Cpanel

Truy cập bằng port 2083

<img src="img/25.png">

## Cài WordPress

Có thể cài WordPress bằng WordPress Toolkit tương tự như bên WHM

<img src="img/26.png">

## Backup/Restore Web

Có thể full backup hoặc backup từng phần như backup thư mục, cơ sở dữ liệu, mail,..

<img src="img/27.png">
<img src="img/28.png">
<img src="img/29.png">

Sau khi hoàn tất quá trình backup sẽ có thông báo được gửi tới email

<img src="img/30.png">

## Quản lý tệp

<img src="img/31.png">
<img src="img/32.png">

## Tạo SubDomain

<img src="img/33.png">

<img src="img/34.png">

## Đổi version PHP

Tại Software => MultiPHP Manager

<img src="img/35.png">

<img src="img/36.png">

