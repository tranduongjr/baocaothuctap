# Các khái niệm cơ bản

- User (người dùng): Để sử dụng Linux, phải có 1 account đăng nhập vào máy linux. Thông tin về tài khoản gồm username, password, các quyền truy xuất tệp tin và thư mục dựa vào tài khoản đăng nhập.
- Group (nhóm): Các người dùng làm việc trên 1 bộ phận hoặc làm việc trên cùng 1 project có thể được đưa vào cùng 1 nhóm
- File (tệp tin): Tất cả các thông tin lưu trữ trên Linux được lưu giữ trong các tệp tin. Các tập tệp tin được tạo ra về người dùng và chủ thể tin có quyền truy xuất, tạo, sửa, thiết lập kích thước tệp tin và phân phối quyền để cho người khác có thể truy xuất tệp tin
- Directory (Thư nục): giống như Folder trong windows. Dùng để chứa tập tin và thư mục khác và tạo ra cấu trúc cho hệ thống tập tin.
- Path (đường dẫn): Là 1 chuỗi các thư mục và có thể kết thúc bằng tên của tập tin. Các thư mục và tập tin được phân cách bởi kí tự /
- Permission (quyền): Là 1 đặc tính quan trọng trong Linux, tạo ra bảo mật bằng cách giới hạn các hành động mà người dùng có thể thực hiện đối với tập tin và thư mục. Các quyền read, Write, execute điều khiển việc truy xuất đối với các truy xuất tới tập tin của người dùng tạo ra nó.
- Process (tiến trình): Khi người dùng thực thi 1 lệnh, Linux tạo ra 1 tiến trình chứa các chỉ thị lệnh. Một tiến trình còn chứa các thông tin điều khiển như thông tin người dùng thực thi lệnh, định danh duy nhất của tiến trình (PID - Process ID).
# 1. Các câu lệnh thường hay sử dụng:
## Thao tác với hệ thống

1. ifconfig : xem ip của máy tính hoặc dùng lệnh #ip a

<img src="img/20.png">

2. uname : Kiểm tra hệ điều hành hiện tại đang sử dụng

<img src="img/21.png">

3. cat /etc/os-release : kiểm tra thông tin bản phân phối của hệ điều hành hiện tại

<img src="img/45.png">

4. date : kiểm tra ngày giờ hiện tại trên máy

<img src="img/22.png">

5. free -m : kiểm tra dung lượng RAM (-m thể hiện biểu diện dưới dạng MB)

<img src="img/23.png">

6. lsblk : hiển thị phân vùng ổ đĩa

<img src="img/46.png">

7. cat /proc/cpuinfo : Xem thông tin CPU

<img src="img/24.png">

8. pwd : hiển thị đường dẫn đến thư mục đang làm việc hiện hành

<img src="img/27.png">

9. hostnamectl : xem thông tin hostname hiện tại của máy 

10. su - : Truy cập vào tài khoản root

11. su - duong :truy cập vào tài khoản duong đã tạo trước đó

<img src="img/25.png">

*Để có thể thay đổi hostname ta có thể sử dụng lệnh #hostnamectl set-hostname "tên hostname muốn đặt"* Để thực thi thay đổi này cần truy cập với tài khoản root. Sau đó chạy lệnh #systemctl restart systemd-hostnamed

12. whoami : kiểm tra người user đang đăng nhập

<img src="img/26.png">

13. history : hiển thị các lệnh đã được thực hiện bởi user hiện tại

<img src="img/28.png">

14. ping + địa chỉ ip : để kiểm tra kết nối

<img src="img/29.png">

15. ps : Liệt kê các tiến trình đang kích hoạt bởi người dùng và PID của tiến trình đó.

<img src="img/30.png">

16. Để tạo user và group thì ta cần thực thi trên tài khoản root:

Dùng lệnh #su - sau đó xác nhận mật khẩu để truy cập root.

<img src="img/31.png">

Tạo account cho user :
```
useradd + Tên user muốn tạo
```
Set password cho account:
```
passwd + Tên user muốn tạo mật khẩu
```

<img src="img/32.png">

Tạo Group:
```
groupadd + Tên Group muốn tạo
```

<img src="img/33.png">

Để thêm user vào group:
```
usermod -a -G +group muốn thêm user vào + tên user muốn thêm vào
```

<img src="img/34.png">

Để xem thông tin về group
```
cat /etc/group
```

<img src="img/35.png">

17. yum update : update hệ thống

<img src="img/43.png">

18. yum install : cài đặt chương trình nào đó

<img src="img/44.png">

19. logout : đăng xuất

20. reboot : khởi động lại

21. shutdown -h now : tắt máy ngay

22. shutdown -h 10 & :lập lịch tắt máy lúc 10h

23. shutdown -r now : khởi động lại

24. init 0 : tắt máy

25. init 6 : khởi động lại máy

**Cấu hình Ip tĩnh**

Dùng lệnh cd /etc/sysconfig/network-scripts để hiển thị những card mạng đang chạy trên máy

<img src="img/101.png">

Ta thấy có card ens33 đang chạy. ta có thể set ip tĩnh cho card đó.

dùng trình soạn thảo Vi để vào chỉnh sửa cấu hình ip

```
vi ifcfg-ens33
```

<img src="img/102.png">

<img src="img/103.png">


thoát và lưu lại.

khởi động lại card mạng bằng lệnh:

```
systemctl restart network.service
```

<img src="img/104.png">

kiểm tra lại thấy ip tĩnh đã được cài đặt

<img src="img/105.png">

## Thao tác với thư mục

26. mkdir : tạo thư mục

<img src="img/36.png">

27. rmdir : Để xóa thư mục và file rỗng

28. rm -rf: xóa mà không cần hỏi lại những thư mục và file không rỗng

29. cd : trỏ đến thư mục đó:

<img src="img/37.png">

30. cat >tenfile.txt : tạo 1 file txt tại thư mục đang trỏ tới.

<img src="img/48.png">

hoặc ta cũng có thể dùng lệnh #touch +tên file để tạo 1 file

<img src="img/51.png">

31. cat : để xem nội dung tệp tin

<img src="img/52.png">

32. Để sửa tệp tin dùng trình soạn thảo vi
cú pháp vi + tên file muốn sửa nội dung

<img src="img/56.png">

<img src="img/57.png">

33. mv : dùng để đổi tên hoặc di chuyển thư mục.

**đổi tên**

cú pháp #mv tencu tenmoi

<img src="img/53.png">

**di chuyển**

cú pháp #mv tenfile thưmụcmuốnchuyểnđến

<img src="img/54.png">

34. ls : liệt kê nội dung của thư mục đang được trỏ tới.

<img src="img/49.png">

35. ls -l : xem quyền được phân trên thư mục đó.

<img src="img/50.png">

36. du -sh : xem dung lượng của thư mục đang được trỏ tới.

<img src="img/40.png">

### Phân quyền cho thư mục.

Phân quyền chia sẻ tài nguyên trên linux xem tại : https://docs.google.com/document/d/1nnxw7OR012pyAQkHc0xy4H-9pcRbSjCR/edit?usp=sharing&ouid=106628548253032794328&rtpof=true&sd=true

## Thao tác với file

37. ls -a : liệt kê các file ẩn

<img src="img/41.png">

#cat : xem nôi dung của file đó. Ví dụ xem file /etc/hosts

<img src="img/42.png">

**Giải nén file**

## Thao tác với trình soạn thảo Vi

- i : (insert) để bắt đầu thao tách ghi, sửa, xóa.
- w : (write) để lưu
- :q! : để thoát
- :wq :để thoát và lưu nội dung đã chỉnh sửa.
- / : để tìm kiếm. Ví dụ /duong
## Thao tác với tường lửa

Các lệnh cơ bản với firewall
~~
systemctl enable firewalld : cho phép tường lửa

systemctl start firewalld : kích hoạt tường lửa

systemctl status firewalld : xem trạng thái tường lửa

systemctl stop firewalld : ngưng tường lửa

systemctl disable firewalld : vô hiệu hóa tường lửa
~~

<img src="img/55.png">

