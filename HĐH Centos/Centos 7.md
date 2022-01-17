# 1. Cài đặt Centos 7

Tiến hành cài file iso Centos 7 tương tự như hướng dẫn tại : https://github.com/tranduongjr/baocaothuctap/blob/main/VM%20ware%20va%20may%20ao/VM%20ware%20va%20may%20ao.md

<img src="img/1.png">

**Lựa chọn ngôn ngữ**

<img src="img/2.png">

**Tiến hành thực hiện các cài đặt**

<img src="img/4.png">

**Cài đặt thời gian, bàn phím,phần mềm,...**

<img src="img/3.png">

**Tiếp theo với cài đặt hệ thống**

Để chia phân vùng ổ cứng, click vào "Installation Destination"

Click vào I will configure partitioning (Tôi sẽ định cấu hình phân vùng)

<img src="img/5.png">

Phân vùng thủ công, chọn LVM trong partitioning scheme 

<img src="img/6.png">

Click vào dấu "+" để lựa chọn tạo các phân vùng như: /, /boot , /swap,...

<img src="img/7.png">

Cấu trúc hệ thống tập tin trong Linux: 

Linux sử dụng cấu trúc hệ thống file có thứ bậc, cáu trúc cây từ trên xuống dưới, với root(/) tại cơ sở của hệ thống file và tất cả các thư mục khác trải ra từ nó.

<img src="img/12.png">

Tùy theo nhu cầu sử dụng người dùng có thể phân vùng cho các thư mục này thủ công tùy ý

- / - Root:

Nó là thư mục gốc chứa các file thư mục khác
Chỉ có Root user mới có thể sử dụng thư mục này
/bin: Lưu trữ tập lệnh thường sử dụng nhất(như sao chép tập tin, tạo thư mục,...)

- /boot: chứa phần nhân khởi động của Linux và file cấu hình khởi động (grub cũng trong thư mục này)

- /dev: chứa các tập tin đặc biệt tương ứng với các thiest bị có trong hệ thống

- /etc: chứa các thiết lập hệ thống

- /home: Chứa các thư mục con có tên ứng với User name của người dùng, mỗi thư mục đó chính là nơi lưu trữ toàn bộ dữ liệu của người dùng.

- /lib: Chứa các thư viện dùng chung của các chương trình (giống file .dll trong windows)

- /tmp: Chứa các file tạm dùng trong quá trình Linux hoạt động

- /usr: Chứa những thứ quan trọng như phần mềm, thư viện hàm, các dữ liệu dùng chung

- /var: chứa các tập tin lưu lại các số liệu biến đổi gồm: hệ thống tập tin log(/var/log), các gói và các file dữ liệu(/var/lib), email(/var/mail), print queues(/var/spool); lock files (/var/lock), các file tạm thời cần khi reboot (/var/tmp)

- /sbin: Chứa các chương trình thực thi nhị phân được yêu cầu bởi System Administrator cho việc bảo trì(iptables, fdisk, ifconfig, reboot, etc)

- /proc: Sử dụng cho nhân Linux. Chúng được sử dụng bởi nhân để xuất dữ liệu sang không gian người dùng

- /otp: thư mục chứa các phần mềm cài thêm

- /mnt và /media Mount point mặc định cho những hệ thống file kết nối bên ngoài

- /srv: dữ liệt được sử dụng bởi các máy chủ lưu trữ trên hệ thống

**Phân vùng "/"** - Root: đây là nơi bắt đầu của tất cả các thư mục, là cơ sở của hệ thống file khác và tất cả các thư mục khác trải ra từ nó:


**/Boot** là phân vùng chứa những file như kernel và các tập tin sử dụng trong boot loader nên chỉ cần để 1GB

<img src="img/10.png">

**/Swap** là phân vùng Ram ảo cho Server, nó sẽ lấy 1 phần dung lượng của ổ cứng để hoạt động khi Ram của Server gần hết hoặc đến ngưỡng do bạn thiết lập trước.

- Đối với server có cấu hình RAM thấp thì sẽ cần dùng đến phân vùng Swap
- Swap thường được đặt gấp đôi RAM vật lý, nếu thiết lập kích thước của swap quá lớn, sẽ gây lãng phí dung lượng mặc dù swap không được dùng.

*Vì máy này Ram cao lên không cần cài nữa*

**Lưu ý**: Hầu hết các file hệ thống này được định dạng với kiểu ext4 vì định dạng này chỉ cho phép Linux mới có quyền truy cập. Còn nếu sử dụng định dạng ổ đĩa ngoài và muốn chia sẻ với các hệ điều hành khác như windows, mac OS,... thì các hệ điều hành này không thể đọc được hệ thống tệp ext4, khi đó nên sử dụng định dạng exFAT hoặc FAT32

Chọn "Done" để hoàn tất quá trình phân vùng ổ đĩa

**Hoàn tất quá trình phân vùng ổ đĩa**

Tiếp theo trong phần Network & Host name chuyển sang chế độ ON để bật kết nối.

<img src="img/13.png">

Click vào Begin Intallation để bắt đầu quá trình cài đặt

<img src="img/14.png">

Cài đặt mật khẩu cho root trong tùy chọn root password

<img src="img/15.png">

Và có thể tạo user trong tùy chọn User creation

Sau đó Reboot lại và truy cập centos với tài khoản mật khẩu root đã tạo trước đó.

Để xem phân vùng ổ cứng đã thực hiện, sử dụng lệnh #lsblk

<img src="img/16.png">

Hoàn tất quá trình phân cài đặt và phân vùng ổ đĩa cho Centos7.

Để cài giao diện Gnome GUI Desktop cho centos 7, có thể tham khảo theo đường link: https://vinasupport.com/cai-dat-giao-dien-gnome-desktop-gui-cho-centos-7-rhel-7/

<img src="img/17.png">
