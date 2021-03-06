# Các thao tác với Zimbra 9

Trang quản trị Mail Server truy cập tại cổng 7071

<img src="img/18.png">

## Quản lý tài khoản

Tại tùy chọn quản lý, nơi quản lý các tài khoản mail người dùng:

<img src="img/22.png">

Các tùy chọn như thêm, sửa, xóa hoặc vô hiệu hóa phiên của một tài khoản mail. Hoặc ta có thể vào tùy chọn xem thư để có thể vào trong webmail của người dùng đó

<img src="img/23.png">

### Gửi nhận mail zimbra

- Đăng nhập vào webmail theo thông tin được người quản trị server gửi ví dụ https://mail.tranduongjr.com

- Nhập user và pass của email sau đó thực hiện sign in:

<img src="img/24.png">

**Gửi mail**

Sau khi đăng nhập chọn Thư mới để tiến hành soạn thảo email mới:

<img src="img/25.png">

Nhập địa chỉ email cần gửi vào phần ``` Tới``` , CC là để tạo bản sao thư và gửi đến 1 người khác, nhập tiêu đề và nội dung thư, có thể đính kèm các tệp sau đó nhấn vào Gửi

<img src="img/26.png">

<img src="img/27.png">

*Lưu ý: Nếu gửi đến nhiều địa chỉ thì các địa chỉ email cách nhau bằng dấu ;*

**Nhận Mail**

Khi có mail mới gửi đến vào phần Hộp thư đến, click vào email sẽ nhìn thấy nội dung email ở bên tay phải

<img src="img/28.png">

### Kiểm tra log gửi nhận mail

Việc kiểm tra log gửi/nhận của email server zimbra là rất cần thiết, giúp xác định được một email đã gửi/nhận thành công hay chưa và nếu chưa thành công thì bị dừng ở bước nào và báo lỗi ra sao.

**Đường dẫn file log**

```
/var/log/zimbra.log
```

**- Chu trình gửi thư**:

Khi click gửi thư => connect tới email server => MTA kiểm tra địa chỉ người nhận => Kiểm tra qua các rule filter, đánh giá spam, virus => Xếp vào queue(queue active) => Gửi thư => Xóa khỏi queue => Thông báo Message accepted for delivery

<img src="img/57.png">

Chu trình nhận: Chấp nhận kết nối từ email server gửi => Kiểm tra qua các rule filter, đánh giá spam, virus => Xếp vào queue (queue active) => Nhận thư và xóa khỏi queue => Thông báo nhận thư (Delivery OK)

<img src="img/58.png">

### Thay đổi domain.

```
su zimbra

zmprov -l rd <domain cũ> <domain mới>
```

Ví dụ:

```
su zimbra

zmprov -l rd mail.tranduongjr.com tranduongjr.com
```

### Thêm domain

Tại trang quản trị mail server zimbra vào tùy chọn Tạo tên miền

<img src="img/67.png">

Tiến hành ghi các thông tin để tạo domain

<img src="img/68.png">

Chọn máy chủ thư và có thể click vào kế tiếp để tiếp tục cấu hình hoặc chọn click hoàn tất (các cấu hình để mặc định)

<img src="img/69.png">

Để quản lý, thêm, sửa, xóa miền nào đó ta có thể thực hiện tại tùy chọn Cấu Hình => Tên miền

<img src="img/70.png">

### Đổi mật khẩu account admin zimbra

Khi cài đặt email server zimbra mặc định sinh ra một account admin có toàn quyền quản trị trên hệ thống email server. Tuy nhiên trong quá trình vận hành sử dụng người quản trị không nhớ được mật khẩu admin nên phải thực hiện thao tác reset password account admin zimbra.

- Truy cập SSH vào email server và chuyển thao tác với user zimbra

```
su zimbra
```

- Kiểm tra những user nào có quyền admin

```
zmprov gaaa
```

- Thay đổi mật khẩu account có quyền admin

```
zmprov sp <admin email address> <mật khẩu mới>
```

<img src="img/29.png">

Lưu ý: Mật khẩu thiết lập phải phù hợp với chính sách mật khẩu được thiết lập

### Thiết lập chính sách mật khẩu

- Login và thao tác trên giao diện trang quản trị mail server zimbra

<img src="img/30.png">

- Thiết lập chính sách mật khẩu

Vào tùy chọn Cấu hình => Default

<img src="img/31.png">

<img src="img/32.png">

Vào tùy chọn Nâng cao và thiết lập các chính sách tương ứng cho mật khẩu

<img src="img/33.png">

Tại tùy chọn này cũng có cách chính sách về đăng nhập thất bại:

<img src="img/34.png">

### Thiết lập quota

Khi tạo một account email trong email server zimbra hệ thống sẽ tự động phân chia quota cho mỗi account theo mặc định. Trong thực tế việc thiết lập quota cho account khác nhau với giá trị khác nhau là cần thiết tùy thuộc vào nhu cầu sử dụng của account đó.

- Vào tùy chọn Quản lý (quản lý tài khoản), sau đó lựa chọn tài khoản muốn chỉnh sửa quota => chuột phải => sửa

<img src="img/35.png">

- Vào tùy chọn nâng cao => Hạn mức

<img src="img/36.png">

**Tùy chỉnh các tham số**

- Giới hạn địa chỉ chuyển tiếp theo người dùng trong phạm vi (ký tự)
- Số lượng tối đa các địa chỉ chuyển tiếp theo người dùng
- Hạn mức tài khoản (MB) (0 là không có giới hạn)
- Số lượng liên hệ tối đa cho phép trong thư mục
- Ngưỡng phần trăm cho các thư cảnh báo hạn mức (%)
- Khoảng thời gian tối thiểu giữa các cảnh báo hạn mức
- Mẫu thư cảnh báo hạn mức

Lưu lại:

<img src="img/37.png">

### Tạo Whitelist / BlackList

- Đăng nhập vào Webmail Zimbra và vào Tùy chọn => Thư

<img src="img/38.png">

Tìm đến Tùy chọn thư rác

<img src="img/39.png">

Để đưa tên miền vào Blacklist: Thêm tên miền hoặc địa chỉ email của địa chỉ gửi thư rác vào ô Chặn các thư gửi từ và chọn nút Thêm. Hoặc có thể xóa địa chỉ email hoặc tên miền tương tự khỏi danh sách.

Để đưa miền vào Whitelist: Thêm địa chỉ email hoặc miền dưới ô Cho phép thư gửi từ và chọn nút Thêm. Hoặc có thể xóa địa chỉ email hoặc miền tương tự khỏi danh sách.

Sau đó lưu lại cấu hình

<img src="img/40.png">

### Thiết lập Forward email zimbra

- Login vào web mail user

<img src="img/60.png">

- Thiết lập Forward:

Vào Tùy chọn => Thư , nhập email muốn nhận bản thư chuyển tiếp và lưu lại cấu hình

<img src="img/61.png">

- Kiểm tra:

<img src="img/63.png">
<img src="img/62.png">

### Thiết lập chữ ký email zimbra

- Login vào web mail user

<img src="img/60.png">

- Thiết lập chữ ký

<img src="img/64.png">

- Kiểm tra

<img src="img/65.png">

### Thiết lập danh sách gửi thư

List mail là tài khoản email chứa các email con để khi ta soạn thư gửi cho list này, nó sẽ tiến hành gửi thư cho tất cả các mail con trong list đó.

Tại trang quản trị của mail server zimbra vào tùy chọn Quản lý => Các danh sách gửi thư và tiến hành tạo danh sách gửi thư.

<img src="img/66.png">

### Bakup/Restore dữ liệu của mail user

Tại trang web mail zimbra => Tùy chọn => Nhập/Xuất

<img src="img/71.png">

### Tìm ID mailbox account trong email zimbra

Mỗi account email trong email server zimbra được đại diện bởi một ID, tuy nhiên ID này sinh ra không theo thứ tự từ nhỏ đến lớn mà sinh ngẫu nhiên. Việc tìm được chính xác tài khoản email nào có ID mailbox là bao nhiêu có thể ứng dụng trong trường hợp restore lại mailbox của một account nào đó.

* Đường dẫn mailbox

```
/opt/zimbra/store/0/
```
* Tìm ID mailbox từ account email

```
su zimbra

zmprov getMailboxInfo <tên email muốn tìm ID>
```

Ví dụ:

```
su zimbra
zmprov getMailboxInfo admin@tranduongjr.com
```

<img src="img/76.png">
