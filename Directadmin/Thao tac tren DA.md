# Các thao tác trên DirectAdmin

## 1. Admin

Gồm các tùy chọn chính là:

- Account Manager
- Server Manager
- Admin Tools
- System Info & File
- Extra Features

### Account Manager

Nơi thực hiện các thao tác quản lý đối với các tài khoản

<img src="img/22.png">

**Add New User**

Thêm các User mới. Mỗi User sẽ được gắn với một User Package. Tại đây phải tạo các package tương ứng cho từng User.

<img src="img/18.png">

Nhập các thông số tương liên quan, cần thiết cho User và sau đó SAVE lại.

<img src="img/19.png">

Để tạo User ta vào tùy chọn Add New User và điền các thông tin tương ứng

<img src="img/20.png">

Xem tất cả các User tại Show All User

<img src="img/21.png">

Ta có thể Send a Message ( gửi tin nhắn), Suspend (đình chỉ), Unsuspend (không sử dụng) hoặc Delete (xóa) một User

<img src="img/23.png">

My Users: xem User đã được tạo

Tại đây còn có thay đổi cấu hình đã cài cho User

<img src="img/24.png">

Manage User Packages: Quản lý các Package của các User

Changer Password: Thay đổi password

Tương tự như add User ta cũng có các tùy chọn để tạo, quản lý  Reseller bao gồm : Create Reseller, List Resellers, Manager Reseller Packages.

<img src="img/25.png">

<img src="img/26.png">

Các tùy chọn để tạo quản lý Administrator: Create Administrator, List Administrator.

Tùy chọn Move Users between Resellers để chuyển đổi các User giữa các Reseller:

<img src="img/27.png">

### Server Manager

**Administrator Settings**

Được chia làm 4 tùy chọn gồm Administrator Settings, Server Settings, Security Settings và E-Mail Settings.

*Administrator Setting*

<img src="img/28.png">

- Thông báo cho tất cả quản trị viên bất cứ khi nào dịch vụ gặp sự cố bằng cách sử dụng hệ thống nhắn tin/vé.

- Bán quá mức: Cho phép Resellers bán nhiều tính năng hơn mức được phép.

- Tạm ngưng Reseller và Người dùng của họ khi Reseller vượt quá giới hạn băng thông của họ.

- Cho phép Resellers sao lưu/khôi phục các Users của họ (Tách biệt với sao lưu/khôi phục Người dùng)

- Cho phép phiên bản DirectAdmin mới nhất được đẩy lên máy chủ này, khi cần thiết.

*Server Settings*

<img src="img/29.png">

*Security Setting*

<img src="img/30.png">

Gồm các tùy chọn để thiết lập bảo mật cho Server như

- Thiết lập Blacklist IPs cho các nỗ lực đăng nhập quá mức hoặc từ các kết nối không được xác thực

- Thời gian trước khi số lần đăng nhập không thành công được đặt lại

- Thiết lập thời gian một IP được gỡ từ blacklist

- Phân tích cú pháp nhật ký dịch vụ cho các cuộc tấn công brute force

- Cảnh báo cho quản trị viên khi một Ip đăng nhập thất bại nhiều lần trên nhiều tài khoản khác nhau hoặc khi một tài khoản bị đăng nhập thất bại nhiều lần từ nhiều IP

- Quét các cuộc tấn công WordPress

- Thực thi chính sách các mật khẩu khó

- Kiểm tra chủ sở hữu miền để tạo miền phụ

*E- Mail Settings*

<img src="img/31.png">

**Custom HTTPD Configurations**

Hiển thị những file httpd.còn của tất cả các tên miền của các user, có thể truy cập để cấu hình theo ý muốn.

<img src="img/32.png">

<img src="img/33.png">

Ngoài ra còn các tùy chọn để quản lý IP (IP Management) quản lý các DNS (DNS Administrator), config PHP, key SSH,...

<img src="img/34.png">

### Admin Tools

**Admin Backup/Transfer**

Backup, Restore data, tại đây có thể thực hiện các hoạt động backup, có thể là lên lịch backup,Restore data,...

<img src="img/35.png">

<img src="img/36.png">

**Brute Force Monitor**

Ghi lại log những lần đăng nhập không thành công

<img src="img/37.png">

Process Monitor: Hiển thị các tiến trình của Server

<img src="img/38.png">

Servive Monitor: Hiển thị các dịch vụ

<img src="img/39.png">

System Backup: cài đặt backup dữ liệu

Message All Users: gửi tin nhắn tới tất cả các User trên DA

### System Info & File

**All User Cron Jobs**

Quản lý các Cron Jobs của các User.

**File Manager**

Quản lý các File

<img src="img/40.png">

**File Editor**

Chỉnh sửa các file của hệ thống

<img src="img/41.png">

**System Information**

Hiển thị thông tin của hệ thống

<img src="img/42.png">

## User

### Account Manager

<img src="img/44.png">

*Domain Setup* : Cấu hình Domain, tại đây có thể chỉnh sửa domain của User, lựa chọn phiên bản PHP cho domain

<img src="img/43.png">

*Subdomain Management* : Quản lý các subdomain

*DNS Management* : Quản lý các bản ghi DNS

*SSL Certificates* : Quản lý chứng chỉ SSL cho domain của user

*FTP Managerment* : Quản lý kết nối FTP

*MySQL Management*: Quản lý các database 

<img src="img/49.png">

*Site redirection* : Chuyển hướng trang web

*PHP Settings* : cài đặt PHP

### Email Manager

<img src="img/45.png">

Quản lý email, Các tài khoản Email, Tự động phản hồi mail, bộ lọc thư rác, bản ghi MX

### Advanced Features

<img src="img/46.png">

*Create/Restore Backups*: Back up hoặc Restore dữ liệu của Site

<img src="img/47.png">

*Cron Jobs*: Tạo các Job tự động

*Custom Error Page* : Tùy chỉnh trang lỗi

*Two-Step Authentication*: Xác thực 2 bước

*Password Protected Directory*: Cấu hình mật khẩu cho các thư viện muốn bảo mật.

### System Info & File

Tương tự như bên Admin cũng gồm quản lý file (File Manager), các thông tin về hệ thống, các modules đã cài đặt.

<img src="img/48.png">

### Extra Features

*phpMyAdmin*: Quản trị database của các site