# Giới thiệu về Plesk

Plesk Control Panel là một trong những phần mềm quản trị hosting phổ biến nhất hiện nay. Nó là giải pháp tổng thể trong việc quản lý máy chủ bao gồm các dịch vụ như web, thư điện tử, cơ sở dữ liệu, tên miền,...

Plesk cung cấp một hệ thống Web lưu trữ bao gồm thanh toán tự động và dự phòng, một Web builder được tích hợp sẵn và có thể truy cập đến hàng trăm ứng dụng trên Web.

## Ưu điểm của Plesk control panel

- **Có thể linh hoạt hoạt động trên 2 hệ điều hành Window & Linux** : Là một hệ thống quản lý máy chủ do Parallels phát triển, nhờ sự linh động và đa dạng hóa trong cơ cấu hoạt động, Plesk có thể hoạt động trên các 2 hệ điều hành thông dụng hiện nay là Windows & Linux. Chính nhờ sự linh động và đa dạng hóa trong cơ cấu hoạt động trên các hệ điều hành thông dụng, Plesk đã phát triển mạnh mẽ và được nhiều doanh nghiệp lựa chọn cho giải pháp quản lý máy chủ

- Nhiều hệ thống phần mềm hữu ích, ổn định, tin cậy.

- Tích hợp đầy đủ các tính năng có thể quản lý các dịch vụ để vận hành cho website của mình.

- Giao diện Plesk thân thiện, dễ sử dụng.

- Đây là phần mềm quản lý hosting duy nhất tích hợp với tính năng thiết kế web, giao diện storefront SaaS và phân hệ Billing, mang đến sự tiện dụng và hiệu quả cho người dùng.

- Thiết lập nhiều host dựa trên gói dịch vụ với cấu hình được định sẵn

- Cho phép tạo nhiều tài khoản FTP, kết hợp với cấu trúc web linh hoạt

## Lợi ích của Plesk

**Có thể phân cấp người sử dụng**

Với 3 cấp độ quản: Administrator, Reseller, End User, Plesk giúp việc quản lý sẽ hiệu quả hơn. Đồng thời, Plesk còn có khả năng bảo mật cực cao khiến người dùng hoàn toàn yên tâm khi sử dụng.

**Hỗ trợ công tác chăm sóc khách hàng**

Người quản trị sẽ không còn bị áp lực về việc hỗ trợ khách hàng nếu chọn Plesk. Các tính năng của một phần mềm quản trị hosting này đã đơn giản hoá cả việc quản lý lẫn việc xử lý sự cố khách hàng. Song song đó, khả năng dịch vụ khách hàng tự quản trị là môt “điểm cộng” mà Plesk thuyết phục đa số người dùng.

**Tự động hóa cao**

Plesk sử hữu nhiều tính năng tự động hóa cao giúp các doanh nghiệp giảm chi phí, thời gian trong việc quản lý, đầu tư thiết bị và nhân lực.

**Tăng doanh thu**

Thông qua Parallels Storefront, đối tác kinh doanh có thể mở rộng các dịch vụ kinh doanh, từ đó, tăng doanh thu trên mỗi khách hàng.
Ví dụ: cung cấp hàng trăm các ứng dụng SaaS.

**Không ngừng đổi mới**

Plesk liên tục làm mới và phát triển không ngừng để tối ưu hoá chất lượng sản phẩm. Plesk phiên bản mới nhất có nhiều tính năng nổi bật hỗ trợ User, Hosters/providers, Developers, các cải tiến khác như  Plesk Updates Manager, new PHP-reated functionality, improved SSL management...

# Cài đặt Plesk

Tiến hành chạy lệnh:

```
sh <(curl https://autoinstall.plesk.com/one-click-installer || wget -O - https://autoinstall.plesk.com/one-click-installer)
```

Sau khi cài xong sẽ có thông báo cài đặt thành công:

<img src="img/3.png">

Truy cập vào trình duyệt với port 8880 hoặc 8443 và đăng nhâp với tài khoản root của vps, lựa chọn ngôn ngữ.

<img src="img/4.png">

Nhập thông tin cấu hình cho tài khoản, nhập mail đã đăng ký trước đó để lấy key, nhập key đã nhận được ở email và chấp nhận các điều khoản

**Tham khảo cách lấy Key dùng thử tại**: https://github.com/tranduongjr/baocaothuctap/blob/main/Plesk/L%E1%BA%A5y%20key.md

<img src="img/5.png">

Tiến hành vào Plesk

<img src="img/6.png">

Chờ cài đặt hệ thống, và click vào Khám phá Plesk

<img src="img/8.png">

Trang chủ của Plesk hiện ra

<img src="img/9.png">

**Thêm tên miền**

<img src="img/12.png">

<img src="img/13.png">

Thông tin miền đã thêm được hiện ra

<img src="img/14.png">

**Tạo tài khoản người dùng**

Vào tùy chọn người dùng và click vào Tạo tài khoản người dùng, sau đó nhập các thông tin tài khoản

<img src="img/15.png">

<img src="img/16.png">
