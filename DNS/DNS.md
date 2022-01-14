# 1. Tổng quan về DNS
## 1.1. DNS là gì?

Hệ thống phân giải tên miền DNS (Domain Name System) là một hệ thống cho phép thiết lập tương ứng giữa địa chỉ IP và tên miền trên Internet.

Hệ thống phân giải tên miền DNS về căn bản là một hệ thống giúp cho việc chuyển đổi các tên miền mà con người dễ ghi nhớ (ví dụ tranduongjr.com) sang địa chỉ IP vật lý (có dạng 192.168.1.1) tương ứng của tên miền đó. DNS giúp liên kết với các trang thiết bị mạng cho các mục đích định vị và địa chỉ hóa các thiết bị trên Internet.

Hệ thống phân giải tên miền phân phối trách nhiệm gán tên miền và lập bản đồ những tên tới địa chỉ IP bằng cách định rõ những máy chủ có thẩm quyền cho mỗi tên miền. Những máy chủ có tên thẩm quyền được phân công chịu trách nhiệm đối với tên miền riêng của họ, và lần lượt có thể chỉ định tên máy chủ khác độc quyền được phân công chịu trách nhiệm đối với tên miền riêng của họ và lần lượt có thể chỉ định tên máy chủ khác độc quyền của họ cho các tên miền phụ.

Hệ thống phân giải tên miền cũng lưu trữ các loại thông tin, chẳng hạn như danh sách các máy chủ email mà chấp nhận thư điện tử cho một tên miền Internet.

## 1.2. Chức năng của DNS

Mỗi website có một tên và một địa chỉ IP. Khi mở một trình duyệt web và nhập tên website, trình duyệt sẽ đến thẳng website mà không cần phải thông qua việc nhập địa chỉ IP của trang web. Quá trình dịch tên miền thành địa chỉ IP để cho trình duyệt hiểu và truy cập được vào website là công việc của 1 DNS server. Các DNS trợ giúp qua lại để phân giải địa chỉ IP thành tên miền (www.example.com) và ngược lại. Người dùng chỉ cần nhớ tên website chứ không cần phải nhớ địa chỉ Ip mỗi khi truy cập.

## 1.3 Cách thức hoạt động

Mỗi nhà cung cấp dịch vụ vận hành và duy trì DNS server riêng của mình, gồm các máy bên trong phần riêng của mỗi nhà cung cấp dịch vụ đó trong Internet. Tức là nếu một trình duyệt tìm kiếm địa chỉ của 1 website thì DNS phân giải tên miền của website này phải là DNS server của chính tổ chức quản lý website đó chứ không phải là của một tổ chức (nhà cung cấp dịch vụ) nào khác.

## 1.4. Cấu trúc của hệ thống tên miền
### 1.4.1. Cấu trúc cơ sở dữ liệu

Cơ sở dữ liệu của hệ thống DNS là hệ thống cơ sở dữ liệu phân tán và phân cấp hình cây.Với Root Server là đỉnh của cây và sau đó các miền (domain) được phân nhánh dần xuống dưới và phân quyền quản lý;. Khi một máy khách (client) truy vấn một tên miền nó sẽ đi lần lượt từ root phân cấp xuống dưới để đến DNS quản lý domain cần truy vấn. Tổ chức  quản lý mức cao nhất của hệ thống tên miền (mức Root) gọi là Top Level Domain (TLD).

Hệ thống tên miền (DNS) cho phép phân chia tên miền để quản lý và nó chia hệ thống tên miền thành zone và trong zone quản lý tên miền được phân chia đó. Các Zone chứa thông tin về miền cấp thấp hơn, có khả năng chia thành các zone cấp thấp hơn và phân quyền cho các DNS server khác quản lý.

Ví dụ: Zone ".com" thì do DNS server quản lý zone ".com" chứa các thông tin về các bản ghi có đuôi là ".com" và có khả năng chuyển quyền quản lý cho các zone cấp thấp hơn cho các DNS khác khác quản lý như "tranduongjr.com" là vùng zone do tranduongjr quản lý.

### 1.4.2. Cấu trúc tên miền (Domain)

- Gốc - Domain root: là đỉnh của nhánh cây tên miền. Nó biểu diễn đơn giản chỉ là dấu "."

- Tên miền cấp cao nhất - Top - Level - Domain: Là gồm vài ký tự xác định một nước, khu vực hoặc tổ chức ví dụ ".com"

- Tên miền cấp 2 (Second level domain) Nó rất đa dạng, có thể là tên một công ty hay một tổ chức, cá nhân,...

- Tên miền cấp nhỏ hơn (Subdomain) Chia thêm ra của tên miền cấp hai trở xuống thường được sử dụng như chi nhánh, phòng ban của một cơ quan hay chủ thế nào đó, ví dụ như hanhchinh.nhanhoa.com là một phòng của công ty Nhân Hòa.

## 1.5. Máy chủ quản lý tên miền (Domain name server)

Máy chủ quản lý tên miền (dns) theo từng khu vực, theo từng cấp như một tổ chức, một công ty hay một vùng lãnh thổ. Máy chủ đó chứa thông tin dữ liệu về địa chi và tên miền trong khu vực, trong cấp mà nó quản lý dùng để chuyển giữa tên mieefnvaf địa chỉ Ip đồng thời nó cũng có khả năng hỏi các máy chủ quản lý tên miền khác hoặc cấp cao hơn nó để có thể trả lời được các truy vấn về những tên miền không thuộc quyền quản lý của nó và cũng luôn sẵn sàng trả lời các máy chủ khác về các tên miền mà nó quản lý.

Máy chủ cáp cao nhất là RootServer do tổ chức ICANN quản lý:

- Là server quản lý toàn bộ cấu trúc của hệ thống tên miền.

- Root Server không chứa dữ liệu thông tin về cấu trúc hệ thống DNS mà nó chỉ chuyển quyền quản lý xuống cho các server cấp thấp hơn và do đó root server có khả năng định đường đến của một domain bất kỳ đâu trên mạng.

## 1.6. DNS Zone

Một domain có thể có nhiều domain con bên trong nó gọi là Subdomain.

Ví dụ domain ".com" có nhiều subdomain như nhanhoa.com, tranduongjr.com,...

Những domain và subdomain mà DNS server quản lý gọi là Zone.

Thông tin của DNS Zones gồm: Tên host và địa chỉ IP được lưu trong DNS server.

DNS cho phép chia hệ thống tên miền thành zone và trong zone quản lý tên miền được phân chia đó.

Các zone chứa thông tin về miền cấp thấp hơn, có khả năng chia thành các zone cấp thấp hơn và phân quyền.

# 2. Các bản ghi DNS (DNS record)
## 2.1. A record.

A record (Address Record) là DNS record cơ bản và quan trọng nhất để truy cập web. Nó giúp trỏ tên miền (domain) của website tới một địa chỉ IP cụ thể.

A record có cú pháp như sau:

[Tên miền] IN A [địa chỉ ip của máy]

ví dụ tranduongjr.com IN A 172.14.255.25

Hầu hết các website chỉ có một bản ghi A, tuy nhiên vẫn cho thể trỏ 1 tên miền đến nhiều địa chỉ IP khác nhau. A record được dùng để chuyển tên miền sang địa chỉ IP. Với IPV6 thì AAAA record sẽ được sử dụng. Cấu trúc bản ghi AAAA cũng giống như bản ghi A.

## 2.2. CNAME Record

CNAME Record (Canonical Name Record) là một bản ghi DNS record quy định một tên miền là bí danh của một tên miền chính khác. Một tên miền chính có thể có nhiều CNAME.

CNAM Record có cú pháp như sau:

[Tên bí danh] IN CNAME [tên miền chính]

Trong đó tên miền chính là tên miền được khai báo trong A record đến ip của máy.

tên bí danh là tên miền khác mà cho phép có thể trỏ tới máy tính (địa chỉ ip) này. Ví dụ www.tranduongjr.com IN CNAME tranduongjr.com tức là  khi nhập tên miền www.tranduongjr.com thì hệ thống cũng sẽ đưa về địa chỉ IP của tên miền chính tranduongjr.com

## 2.3. MX Record

MX (Mail Exchange) record là một bản ghi DNS giúp xác định mail server mà email sẽ được gửi tới. Một tên miền có thể có nhiều MX record, điều này giúp tránh việc không nhận được email nếu một mail server ngưng hoạt động.

MX có cú pháp đơn giản ví dụ như: 

tranduongjr.com IN MX 10 mx20.tranduongjr.com

tranduongjr.com IN MX 20 mx20.tranduongjr.com

10,20,... là giá trị ưu tiên, các số càng nhỏ thì độ ưu tiên càng cao. Trong ví dụ trên thì các mail có cấu trúc ....@tranduongjr.com sẽ được gửi tới mail server mx10.tranduongjr.com. Nếu có lỗi xảy ra thì mail sẽ được chuyển tới mail server mx20.tranduongjr.com.

## 2.4. TXT record

TXT record là một loại DNS record giúp tổ chức các thông tin text của một tên miền. Một domain có thể có nhiều bản ghi TXT và chúng chủ yếu được dùng cho các Sender Policy Framework (SPF), Giúp email server xác định được thư được gửi đến có phải từ một nguồn đáng tin hay không. Ngoài ra loại ghi DNS còn dùng để xác thực máy chủ của một tên miền, xác minh SSL,...

## 2.5. NS record.

NS (Name Server) Record là một loại DNS record gúp các định thông tin của moojt tên miền cụ thể được khai báo và quản lý trên máy chủ nào.

Cú pháp của NS record:

[tên miền] IN NS [tên máy chủ tên miền]

ví dụ: tranduongjr.com IN NS ns1.zonedns.vn hoặc tranduongjr.com IN NS ns4.zonedns.vn,...

Trong ví dụ trên, tên miền tranduongjr.com sẽ được quản lý bởi hai máy chủ tên miền là ns1.zonedns.vn và ns4.zonedns.vn. Điều này cũng có nghĩa là các DNS record (A record, MX record, CNAME record,...) của tên miền tranduongjr.com sẽ được khai báo trên máy chủ này.

## 2.6 PTR record

PTR (point) Record có thể nói là 1 DNS record ngược lại với A record. Nó chuyển đổi từ địa chỉ IP sang tên miền. Bản ghi PTR giúp xác thực IP của các hostname gửi tới, giúp hạn chế spam mail.

Ngoài 6 loại record trên vẫn còn các loại bản ghi DNS khác ít phổ biến như SOA record, SRV record, APL record, CAA record, NAPTR record,... 