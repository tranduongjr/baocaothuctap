# 1. Giới thiệu về DirectAdmin
## 1.1. DirectAdmin là gì?

DirectAdmin là công cụ quản trị Server (Web hosting control panel) được phát triển để dễ dàng thực hiện công việc hằng ngày của webmaster, đặc biệt là những người có ít hoặc không có kinh nghiệm trước đó. DirectAdmin được sử dụng thông qua trình duyệt web, có giao diện trực quan và rất dễ sử dụng. 

Phần mềm DirectAdmin cung cấp cho người dùng nhiều tính năng như quản lý domain, subdomain, DNS, FTP và cơ sở dữ liệu MySQL. Không những vậy, khi sử dụng DirectAdmin cũng có thể tạo thêm được các email theo tên miền, tạo SSH key, bảo mật SSL,... Với DirectAdmin, người dùng sẽ dễ dàng upload và quản lý với các file với File Manager một các nhanh chóng và dễ dàng.

## 1.2 Ưu điểm và nhược điểm
### Ưu điểm

Về cơ bản, DirectAdmin có một số đặc điểm đáng chú ý mà chắc chắn có thể khiến khách hàng tiềm năng phải trầm trồ, mặc dù không phải duy nhất nhưng đó là những lĩnh vực mà DA vượt trội và cải thiện rất nhiều với mỗi phiên bản trước.

- Giao diện đồ họa tuyệt vời (GUI): DA đem lại sự đơn giản trong giao diện, Thay vì quá nhiều phần và tùy chọn, tất cả các tính năng được sắp xếp chồng lên nhau dưới ba nhánh chính: Trình quản lý tài khoản, trình quản lý email và tính năng bổ sung. Các tính năng bổ sung có thể nhìn thấy rõ ràng và hầu hết chúng đều tự giải thích ngay cả trước khi nhấp vào chúng.

- Gói đăng ký giá cả phải chăng: Giá cả hợp lý là điều vẫn giữ cho DA cạnh tranh trong khi thị trường nơi tồn tại các giải pháp hoàn hiện hơn nhiều. DA cũng cung cấp một tài khoản dùng thử miễn phí

- Hỗ trợ: Ngoài sự hỗ trợ của nhà cung cấp dịch vụ lưu trữ, chúng ta cũng có thể nhận được sự hỗ trợ trực tiếp từ các kỹ thuật viên của DA. Người dùng trên gói Lite và Standard có thể được hưởng lợi từ hệ thống ticket bên trong bảng điều khiển. Bằng cách này, nếu có vấn đề với DA và các hoạt động của nó - Chúng ta có thể nhận trợ giúp trực tiếp.

- Phục hồi sự cố tự động: Một điều tuyệt vời của DA là tính ổn định của các dịch vụ. Nếu có sự cố bất ngờ xảy ra, trước tiên DA sẽ thử khởi động lại dịch vụ để xem liệu điều này có khắc phục được sự cố hay không. Nếu điều đó là không hiệu quả - hệ thống sẽ gửi thông báo khẩn cấp đến quản trị viên web, giúp họ giải quyết vấn đề trong thời gian thích hợp.

- Tốc độ: DA được thiết kế tương đối nhẹ và nhanh. Việc tải các tài nguyên từ DA cũng vô cùng thấp.

- Giao diện quản trị: DA sở hữu một giao diện đơn giản, dễ dàng sử dụng và quản lý.

- Hỗ trợ nhiều phân cấp user: Hệ thống phân cấp người dùng hỗ trợ tốt cho việc quản trị người dùng và đối tượng người dùng. Vì thế, DA phù hợp với các đơn vị cung cấp hosting cho nhiều người dùng trực thuộc thông qua tài khoản reseller.

- Manual configuration: DA cung cấp hầu hết các tính năng thông qua giao diện website, nhưng người dùng cũng có thể config thủ công bằng cách sử dụng command line. Thực tế, nhiều admin quản trị server thích sử dụng cách này hơn so với việc sử dụng giao diện web.

### Nhược điểm

- Khả năng thêm các chức năng: Về mặt này thì DA còn rất hạn chế. Tuy nhiên, vẫn có thể thêm các chức năng nhưng sẽ tốn thêm chi phí cho việc này.

- Cộng đồng người dùng ít

- Giao diện khá nâng cao với người dùng: Người dùng mới có thể gặp khó khăn trong việc tìm kiếm tính năng cần sử dụng. DA được phân chia thành nhiều cấp và nó mất thời gian để xác định vị trí tính năng mình cần.

## 1.3 Các tính năng chính của DA

### Chức năng của Administrator trong DA

1. Create /Modify Admins and Reseller:

- Admin có thể tọa Reseller hoặc tạo bổ sung 1 admin mới một cách nhanh chóng và dễ dàng

2. Reseller Package:

- Admin có thể tạo các gói tài khoản với các thông số được xác định trước bằng cách sử dụng tính năng này. Đến khi tạo tài khoản, Admin chỉ cần chọn một gói thay vì theiest lập thủ công từng tính năng cho tài khoản.

3. Show all Users:

- Tính năng này cho phép Admin xem nhanh tất cả các tài khoản trên hệ thống và sắp xếp danh sách này theo nhiều cách khác nhau.

4. DNS Administrator: 

- Cho phép Admin tạo, sửa đổi hoặc xóa bất kỳ bản ghi DNS nào trên máy chủ.

5. IP Manager:

- Đây là nơi Admin đặt địa chỉ IP có sẵn cho máy chủ. Admin cũng có thể phân bổ địa chỉ IP cho Reseller từ menu này.

6. Mail Queue Administration:

- Công cụ để xem danh sách mail và message. Bao gồm các công cụ để thực hiện hành động đối với các message đó.

7. System/Services Info:

- Admin có thể xem, dừng và bắt đầu hoặc khởi động lại các dịch vụ từ menu này.

8. Complete Usage Statistics:

- Tính năng này cung cấp cho Admin một cái nhìn tổng quan đầy đủ về việc sử dụng hệ thống. Đầu vào và đầu ra chính xác từ Card Ethernet của máy chủ cũng được giám sát.

9. DNS Clusting:

- DirectAdmin giao tiếp với các máy DirectAdmin để khác để tự động chuyển dữ liệu DNS giữa chúng. Nó có khả năng kiểm tra máy chủ khác để tìm tên miền và không cho phép các tên miền trùng lặp trên DA của bạn.

10. SPAM  fighting tools in DirectAdmin:

- Các công cụ chống Spam được cung cấp bởi DA

11. Licensing / Update: 

- Admin có thể xem trạng thái giấy phép của mình và tải xuống các bản nâng cấp phần mềm và bảo mật DA mới nhất.

### Chức năng của Reseller trong DirectAdmin

1. Create / List / Modify Accounts:

- Việc tạo, liệt kê, sửa đổi và xóa tài khoản được thực hiện nhanh chóng và dễ dàng.

2. User Packages:

- Reseller có thể tạo các Packages được xác định trước bằng cách sử dụng tính năng này. Khi tạo tài khoản, Reseller chỉ cần chọn một Package thay vì thiết lập từng tính năng tài khoản theo cách thủ công.

3. Reseller Statistics:

- Reseller được cung cấp thông tin tổng quan đầy đủ về tổng mức sử dụng của họ. Reseller cũng có thể sắp xếp dữ liệu theo user để nhanh chóng đánh giá tình hình tổng thế.

4.  Message All Users:

- Reseller có thể nhanh chóng gửi tin nhắn tới tất cả khách hàng của họ bằng cách sử dụng hệ thống hỗ trợ ticket được tích hợp sắn của DirectAdmin.

5. Import / Manager Skins:

- Với tùy chọn menu này, Reseller có thể nhanh chóng import và áp dụng giao diện chỉ bằng 1 nút bấm.

6. IP Assignment:

- Reseller có thể phân bổ địa chỉ IP cho khách hàng của họ bằng cách sử dụng tùy chọn menu này.

7. System / Service Information:

- Bằng cách nhấp vào tính năng này, Reseller có quyền truy cập tức thì vào trạng thái của máy chủ và thông tin hệ thống. 

8. Name Servers:

- Reseller có thể tạo nameservers được cá nhân hóa cho khách hàng của họ từ menu này.

### Chức năng của User trong DirectAdmin

1. Email Administration

- User có thể tạo tài khoản POP/IMAP, địa chỉ email, forwarder, danh sách gửi thư, thư trả lời tự động và webmail, bộ lọc cho phép người dùng chặn mail theo tên miền, từ khóa và kích thước.

2. FTP Managerment

- User có thể tạo tài khoản FTP và thiết lập quyền thư mục cho từng tài khoản. FTP ẩn danh cũng được hỗ trợ.

3. DNS menu

- User có thể thêm và xóa các bản ghi, thay đổi cài đặt MX và bất kỳ thứ gì khác với toàn quyền kiểm soát DNS

4. Statistics menu

- User có sẵn mọi thống kê về tài khoản của họ. Các tùy chọn nâng cao hơn và Webalizer cũng được bao gồm

5. Subdomain Menu:

- User có thể liệt kê, tạo, xóa và lấy số liệu thống kê về các subdomains.

6. File manager

- Một sự thay thế nhanh chóng và thân thiện với người dùng cho FTP. Bao gồm mọi tính năng cần thiết để xây dựng và duy trì một trang web.

7. MySQL Databases:

- User có thể dễ dàng tạo, sửa đổi và xóa cơ sở dữ liệu MySQL từ menu này.

8. Site Backup

- Sử dụng công cụ hữ ích này, User có thể sao lưu và khôi phục những gì họ muốn.

9. Error Pages:

- User có thể tạo các thông báo và kết quả đầu ra tùy chỉnh cho các mã lỗi 401, 403, 404 và 500

10. Directory Password Protection:

- User có thể cài đặt mật khẩu bảo vệ bất kỳ thư mục nào bằng tên username và password

11. PHP Selector

- Cho phép khách hàng chọn phiên bản PHP nào sẽ được liên kết với phần mở rộng php.

12. Advanced Tools

- User có thể cài đặt chứng chỉ SSL, xem thống tin máy chủ và các mô đun perl đã cài đặt, đặt cronjob, mime types và trình xử lý apache, đồng thời cho phép chuyển hướng trang web và trỏ tên miền.

### Chức năng chung trong DirectAdmin

1. Intergrated Ticket Support System

- Với hệ thống tích hợp hỗ trợ ticket của DA, bạn sẽ được cung cấp dịch vụ hỗ trợ khách hàng tốt hơn và ít rắc rối hơn. "Bạn có XX tin nhắn đang chờ" được hiển thị mỗi khi đăng nhập và bạn có thể đặt DA thông báo cho bạn về các yêu cầu hỗ trợ qua email, đảm bảo rằng không có yêu cầu nào bị bỏ qua. Nếu bạn muốn cung cấp hỗ trợ theo một cách khác, chỉ cần tắt tính năng này.

2. Two - Factor Authentication

-  Cho phép bất kỳ tài khoản DA nào yêu cầu xác thực 2 yếu tố bằng mã từ ứng dụng trên smartphone

3. Plugin System

- Cho phép mở rộng chức năng DA một cách dễ dàng.

4. Live Updates

- Quản trị viên máy chủ có thể nhấp vào nút "licensing / updates" để xem trạng thái phiên bản và giấy phép hiện tại. Không cần phải tải xuống, giải nén và cài đặt theo cách thủ công - DA tự động thực hiện tất cả các bản cập nhật.

5. Completely Customizable

- DA được thiết kế để trở lên độc đáo như doanh nghiệp của bạn. Mọi khía cạnh của giao diện DA đều có thể được thay đổi và các thiết kế mới được import dễ dàng thông qua menu "skin"

6. Automatic Recovery From Crashes

- DirectAdmin Task Queue đảm bảo rằng tất cả các dịch vụ luôn hoạt động. Nếu có sự cố, DirectAdmin sẽ cố gắng khắc phụ sự cố băng cách khởi động lại dịch vụ. Nếu không thành công, DA sẽ thông báo cho quản trị viên máy chủ ngay lập tức.

7. We support your customers through site-helper

- Được thiết kế để giúp người quản trị và khách hàng sử dụng DA

# 2. Cài đặt DirectAdmin trên Centos 7

## 1. Đăng ký tài khoản DirectAdmin

Vào trang chủ DirectAdmin để đăng ký tài khoản và license dùng thử :

https://www.directadmin.com/

<img src="img/1.png">

Submit xong ta sẽ nhận được usr ID và Password được gửi về gmail:

<img src="img/2.png">

Ta sử dụng tài khoản được cấp để đăng nhập vào và lấy key

<img src="img/3.png">

Create a Trial

<img src="img/4.png">

<img src="img/5.png">

## Cài đặt DirectAdmin

Cài các gói cần thiết cho DirectAdmin

```
yum install wget gcc gcc-c++ flex bison make bind bind-libs bind-utils openssl openssl-devel perl quota libaio
libcom_err-devel libcurl-devel gd zlib-devel zip unzip libcap-devel cronie bzip2 cyrus-sasl-devel perl-ExtUtils-Embed
autoconf automake libtool which patch mailx bzip2-devel lsof glibc-headers kernel-devel expat-devel

yum install psmisc net-tools systemd-devel libdb-devel perl-DBI xfsprogs rsyslog logrotate crontabs file
```

<img src="img/6.png">

<img src="img/7.png">

Tải gói DirectAdmin về cài đặt

```
wget http://www.directadmin.com/setup.sh && chmod 755 setup.sh

./setup.sh
```

Nhập license key đã lấy được ở bước Create a Trial bên trên.

<img src="img/9.png">

Thông báo cài đặt thành công và có thể truy cập vào DirectAdmin theo port 2222 với username và password được cấp

<img src="img/11.png">

<img src="img/10.png">

Trang quản trị DirectAdmin hiện ra

<img src="img/12.png">