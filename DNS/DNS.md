# 1. Tổng quan về DNS
## 1.1. DNS là gì?

Hệ thống phân giải tên miền DNS (Domain Name System) là một hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet.

Hệ thống phân giải tên miền DNS về căn bản là một hệ thống giúp cho việc chuyển đổi các tên miền mà con người dễ ghi nhớ (ví dụ tranduongjr.com) sang địa chỉ IP vật lý (có dạng 192.168.1.1) tương ứng của tên miền đó. DNS giúp liên kết với các trang thiết bị mạng cho các mục đích định vị và địa chỉ hóa các thiết bị trên Internet.

Hệ thống phân giải tên miền phân phối trách nhiệm gán tên miền và lập bản đồ những tên tới địa chỉ IP bằng cách định rõ những máy chủ có thẩm quyền cho mỗi tên miền. Những máy chủ có tên thẩm quyền được phân công chịu trách nhiệm đối với tên miền riêng của họ, và lần lượt có thể chỉ định tên máy chủ khác độc quyền được phân công chịu trách nhiệm đối với tên miền riêng của họ và lần lượt có thể chỉ định tên máy chủ khác độc quyền của họ cho các tên miền phụ.

Hệ thống phân giải tên miền cũng lưu trữ các loại thông tin, chẳng hạn như danh sách các máy chủ email mà chấp nhận thư điện tử cho một tên miền Internet.

## 1.2. Chức năng của DNS

Mỗi website có một tên và một địa chỉ IP. Khi mở một trình duyệt web và nhập tên website, trình duyệt sẽ đến thẳng website mà không cần phải thông qua việc nhập địa chỉ IP của trang web. Quá trình dịch tên miền thành địa chỉ IP để cho trình duyệt hiểu và truy cập được vào website là công việc của 1 DNS server. Các DNS trợ giúp qua lại để phân giải địa chỉ IP thành tên miền(www.example.com) và ngược lại. Người dùng chỉ cần nhớ tên website chứ không cần phải nhớ địa chỉ Ip mỗi khi truy cập.

# 2. Các bản ghi DNS (DNS record)
# 2.1.