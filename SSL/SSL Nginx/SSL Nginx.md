# 1. Giới thiệu
## SSL là gì?
- SSL là chữ viết tắt của Secure Socket Layer (lớp bảo socket bảo mật). Một loại bảo mật giúp mã hóa liên lạc giữa website và trình duyệt. 

- Chức năng chính của SSL là bảo vệ thông tin và giao tiếp giữa máy khách và máy chủ. Giao tiếp này chủ yếu liên quan tới các trang web trên HTTP, email, và SSL đảm bảo mã hóa và giải mã các thông điệp được chuyển giữa các máy chủ này.

- SSL cho phép các trang web bảo mật vì nó loại bỏ bất kỳ người trung gian nào trên mạng. Nó cũng cung cấp một đường truyền thông tin liên lạc an toàn, nơi khách hàng có thể truyền thông tin đến và đi từ một trình duyệt mà không bị can thiệp.

## Hoạt động của SSL

Hai hệ thống mã hóa chi phối cách SSL hoạt động là:

- Mã hóa khóa bất đối xứng
- Mã hóa khóa đối xứng

Mã hóa khóa bất đối xứng hay còn gọi là mật mã khóa công khai. Trong mật mã bất đối xứng, có 2 cặp khóa là khóa công khai và khóa riêng. Cả hai đều tham gia vào quá trình mã hóa hoặc giải mã dữ liệu.

Trong mã hóa bất đối xứng thì một khóa được gán cho một trong hai bên ở đầu kia một khóa công khai. Khóa còn lại là khóa riêng được dùng để mã hóa dữ liệu và các bên không xác định được. Dữ liệu được xử lý bằng khóa riêng để mã hóa và giải mã bằng khóa công khai.

Trong mã hóa khóa đối xứng thì chỉ có một khóa có sẵn cho cả máy khách và máy chủ. Khóa này mã hóa và giải mã dữ liệu.

SSL sử dụng cả mã hóa bất đối xứng và mã hóa đối xứng để truyền dữ liệu một cách an toàn

## Cách truyền dữ liệu quá SSL

Giao tiếp giữa máy chủ và máy khách được ví như bắt đầu bằng một cái bắt tay. khi bắt đầu, trình duyệt cố gắng giao tiếp với máy chủ web. Trong SSL sự bắt đầu này sử dụng mã hóa khóa bất đối xứng. Khi bắt đầu :

- Trình duyệt xác minh tính xác thực của máy chủ.
- Trình duyệt và máy chủ mở một kết nối an toàn để liên lạc.
- Trình duyệt và máy chủ tạo khóa phiên.

Trong quá trình truyền dữ liệu, máy khách và máy chủ chia sẻ một khóa để mã hóa và giải mã dữ liệu. Quá trình này là mã hóa khóa đối xứng.

## Chứng thư số SSL

SSL thực tế là một tệp chứa khóa công khai cho trang web. Nó nằm trên máy chủ của trang web và nếu không có nó, không thể thực hiện kết nối an toàn được. Nhờ có nó mà máy khách khi truy cập có thể xác minh được tính xác thực, tin cậy của website, đảm bảo mọi dữ liệu, thông tin trao đổi giữa máy chủ và máy khách luôn được bảo mật và an toàn.

Chứng thư số SSL được cấp bởi CA (tổ chức phát hành chứng thư số). Trước tiên, CA sẽ xác minh danh tính và tính hợp pháp của chủ sở hữu trang web trước khi tiến hành cấp chứng thư số SSL.

Let's Encrypt là một tổ chức xác thực SSL giống như Comodo, Geotrust, Symantec nhưng cái khác là Let's Encrypt là một tổ chức phi lợi nhuận được thành lập với sự bảo trợ của những tổ chức lớn trên thế giới như Cisco, Akamai, Mozilla, Facebook,... với mục đích là cung cấp chứng thư số SSL miễn phí cho mọi người, giúp mọi website đều được mã hóa, tạo lên môi trường Internet an toàn hơn

Có 2 cách tạo SSL:

- Nhờ một tổ chức CA (Certification Authority) cấp, là tổ chức có độ tin cậy cao, được quyền cấp và chứng nhận SSL. Sẽ mất phí.
- Self - Signed SSL: Là server tự cấp, tự kí, tự xác thực (không an toàn và tin tưởng bằng nhờ bên thứ 3). Với cách này thì không mất phí.

# 2. Chuẩn bị

Một Webserver Nginx chạy trên hệ điều hành Centos 7

Tham khảo cách cấu hình Nginx trên centos 7 tại:

https://github.com/tranduongjr/baocaothuctap/blob/main/Nginx/Nginx.md

# 3. Cài đặt SSL cho Nginx