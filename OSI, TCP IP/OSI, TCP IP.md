# 1. Tổng quan về các mô hình.
## 1.1. Mô Hình OSI và TCP/IP

  Trong mạng máy tính, để truyền tải dữ liệu giữa các người dùng với nhau thì cần có một phương pháp nào đó mang tính hệ thống. Phương pháp này sẽ giúp truyền tải dữ liệu theo quy tắc nhất định, tạo điều kiện cho dữ liệu truyền đi trên môi trường mạng một cách mượt mà, có hệ thống.

![mô hình OSI và TCP IP](https://user-images.githubusercontent.com/97416839/148732516-81e2e0f2-4034-4040-a929-22b9850cf9d8.jpg)

### 1.1.1. Mô hình OSI.
  Mô hình OSI (Opera Systems Interconnection) là mô hình giúp kết nối giữa các thiết bị Internet trên toàn cầu. Mô hình này có kiến trúc phân tầng, gồm 7 tầng với những chức năng riêng biệt của từng tầng như mô hình sau: 

![osi](https://user-images.githubusercontent.com/97416839/148745010-b22a1743-c9bc-43f8-aa71-33db19bcd959.png)

#### a, Tầng vật lý (Physical Layer).

  Tầng này đảm bảo các vấn đề về các thiết bị vật lý liên quan tới quá trình định tuyến mạng. Xác định các chức năng, thủ tục về điện, cơ, quang để kích hoạt, đảm bảo cho quá trình truyền tải dữ liệu được hiệu quả nhất.
  Ở tầng này thì dữ liệu được truyền đi dưới dạng bit 0 và 1. 

#### b, Tầng liên kết dữ liệu (Data Link Layer).

  Đáp ứng các nhu cầu về tầng mạng và phát sinh các yêu cầu phục vụ gửi tới tầng vật lý. Đảm bảo truyền tải các khung dữ liệu (Frame) giữa hai máy tính có đường truyền vật lý nối trực tiếp với nhau là điều mà chúng thực hiện. Ngoài ra nó còn cài đặt cơ chế phát hiện và xử lý lỗi dữ liệu nhận.

#### c, Tầng mạng (Network Layer).

  Đáp ứng các nhu cầu về tầng vận chuyển. Tầng mạng đảm nhiệm việc truyền các gói tin (packet) giữa hai máy tính bất kỳ trong mạng máy tính.

#### d, Tầng vận chuyển (Transport Layer).

  Vai trò của chúng là phân mảnh các gói tin có kích thước lớn khi gửi và tập hợp chúng khi nhận, quá trình phân mảnh khi gửi và nhận đảm bảo tính toàn vẹn cho dữ liệu (không bị mất mát, không lặp và đúng thứ tự).
  => Khi A muốn gửi dữ liệu cho bên B. 1 kết nối được thiết lập giữa A và B, bên máy A gửi dữ liệu sử dụng cơ chế phân mảnh thì bên máy B sẽ nhận dữ liệu theo đúng trật tự ban đầu bên gửi.
  Tại tầng này, dữ liệu truyền đi và nhận về sẽ được kiểm soát luồng và kiểm soát lỗi để đảm bảo dữ liệu truyền đi được chính xác và không quá tải cho bên nhận.

#### e, Tầng phiên (Session).

  Tầng này tạo ra và duy trì một phiên cho quá trình truyền tải dữ liệu giữa hai thiết bị. Nó chịu trách nhiệm cho việc đóng, mở luồng cho quá trình giao tiếp giữa 2 thiết bị với nhau, đảm bảo rằng phiên mở đủ lâu để dữ liệu có thể truyền tải hết và đóng đủ nhanh để tránh lãng phí tài nguyên.
  Tầng phiên còn đánh dấu điểm hoàn thành. Ví dụ khi truyền 1 file 10gb dữ liệu. Sau mỗi 1gb được truyền đi thì sẽ được đánh dấu điểm hoàn thành tại đó. Nên khi có sự cố đường truyền tại điểm 5gb thì khi có kết nối lại sẽ tiếp tục truyền từ điểm 5gb đến khi truyền hết 10gb.

#### f, Tầng trình bày (Presentation Layer).

  Đáp ứng các yêu cầu của tầng ứng dụng như phiên dịch, giải mã, mã hóa và nén dữ liệu trước khi đưa xuống tầng phiên.
  
  Tại tầng này, dữ liệu được phiên dịch thành ngôn ngữ mà ứng dụng có thể hiểu được,
#### g, Tầng ứng dụng.

  Là tầng đầu tiên của mô hình OSI, tầng này cung cấp giao diện cũng như các thao tác dữ liệu giúp người dùng tương tác trực tiếp với ứng dụng. Thông qua các phần mềm sẽ giúp cho người dùng truy cập các thông tin và dữ liệu trên mạng. Một số giao thức hoạt động tại tầng này như HTTP, FTP, POP, IMAP, SMTP, SNMP,TCP, DNS,.... Một số ứng dụng về tầng này như Web, Mail,...
### 1.1.2. Mô hình TCP/IP.
Mô hình TCP/IP (Transmission Control Protocol/Internet Protocol) là giao thức truyền thông được sử dụng để kết nối các thiết bị với nhau thông qua mạng Internet.
Bộ giao thức TCP/IP hoạt động như một lớp trìu tượng giữa các ứng dụng Internet và hạ tầng Router/Switch.

![mô hình tcp](https://user-images.githubusercontent.com/97416839/148893792-d3943f04-89a3-4e6d-80d4-54977cab9c01.png)

TCP/IP là sự kết hợp của 2 giao thức là TCP (Giao thức truyền vận) đóng vai trò kiểm tra và đảm bảo sự an toàn của mỗi gói tin khi đi qua mỗi trạm. Trong quá trình này, nếu giao thức TCP nhận được gói tin bị lỗi thì một tín hiệu được truyền đi và yêu cầu hệ thống gửi lại một gói tin khác. Và giao thức IP (Giao thức liên mạng) cho phép các gói tin được gửi đến đích định sẵn bằng cách gán thông tin đường dẫn cho các gói tin để gói tin có thể đến được đích đã định sẵn ban đầu.
Mô hình TCP/IP gồm 4 tầng:
#### a, Tầng ứng dụng (Application)
Đây là lớp giao tiếp trên cùng của mô hình. Đúng với tên gọi, tầng Ứng dụng đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chat, gửi email, một số giao thức trao đổi dữ liệu: SMTP, SSH, FTP,...)
Các dữ liệu khi tới tầng này sẽ được định dạng để kết nối theo kiểu Byte nối Byte. Các thông tin định tuyến tại đây sẽ giúp xác định đúng đường đi của một gói tin.
#### b, Tầng giao vận (Transpot Layer).
Chức năng chính của tầng 3 là xử lý vấn đề giao tiếp giữa các máy chủ trong cùng một mạng hoặc khác mạng được kết nối với nhau thông qua bộ định tuyến. Tại đây dữ liệu sẽ được phân đoạn, mỗi đoạn sẽ không bằng nhau nhưng kích thước phải nhỏ hơn 64KB. Cấu trúc đầy đủ của một Segment lúc này là Header chứa thông tin điều khiển và sau đó là dữ liệu.

Trong tầng này còn bao gồm 2 giao thức cốt lõi là TCP và UDP.

* Giao thức TCP:
* 
    TCP là giao thức truyền tải hướng kết nối (connection-oriented), nghĩa là phải thực hiện thiết lập kết nối với đầu xa trước khi thực hiện truyền dữ liệu. Tiến trình thiết lập kết nối ở TCP được gọi là tiến trình bắt tay 3 bước (threeway handshake).
    
    Cung cấp cơ chế báo nhận (Acknowledgement) :Khi A gửi dữ liệu cho B, B nhận được thì gửi gói tin cho A xác nhận là đã nhận. Nếu không nhận được tin xác nhận thì A sẽ gửi cho đến khi B báo nhận thì thôi.
    
    Cung cấp cơ chế đánh số thứ tự gói tin (sequencing) cho các đơn vị dữ liệu được truyền, sử dụng để ráp các gói tin chính xác ở điểm nhận và loại bỏ gói tin trùng lặp.
    
    Có các cơ chế điều khiển luồng thích hợp (flow control) để tránh nghẽn xảy ra.
    
    Hỗ trợ cơ chế full-duplex ( truyền và nhận dữ liệu cùng một lúc)
    
    Phục hồi dữ liệu bị mất trên đường truyền ( A gửi B mà không thấy xác nhận sẽ gửi lại) .
    
* Giao thức UDP:

    Ngược lại với giao thức TCP thì UDP là giao thức truyền tải hướng không kết nối (connectionless). Nó sẽ không thực hiện thao tác xây dựng kết nối trước khi truyền dữ liệu mà thực hiện truyền ngay lập tức khi có dữ liệu cần truyền (kiểu truyền best effort) => truyền tải rất nhanh cho dữ liệu của lớp ứng dụng.
    
    Không đảm bảo tính tin cậy khi truyền dữ liệu và không có cơ chế phục hồi dữ liệu ( nó không quan tâm gói tin có đến đích hay không, không biết gói tin có bị mất mát trên đường đi hay không) => dễ bị lỗi.
    
    Không thực hiện các biện pháp đánh số thứ tự cho các đơn vị dữ liệu được truyền…
    
    Nhanh và hiệu quả hơn đối với các dữ liệu có kích thước nhỏ và yêu cầu khắt khe về thời gian.
    
    Bản chất không trạng thái nên UDP hữu dụng đối với việc trả lời các truy vấn nhỏ với số lượng lớn người yêu cầu.
**So sánh phân biệt TCP và UDP**

*Giống nhau*

    Đều là các giao thức mạng TCP/IP hoạt động tại tầng giao vận (Transpot Layer)
    
*Khác nhau*

TCP:Hướng kết nối, độ tin cậy cao, gửi dữ liệu dạng luồng byte, không cho phép mất gói tin, đảm bảo việc truyền dữ liệu, có sắp xếp thứ tự các gói tin, tốc độ truyền dữ liệu thấp

UDP: Hướng không kết nối, Độ tin cậy thấp, gửi dữ liệu theo datagram, cho phép mất gói tin, không đảm bảo việc truyền dữ liệu, không sắp xếp thứ tự các gói tin, tốc độ truyền dữ liệu cao

=> Tùy thuộc vào yêu cầu của từng ứng dụng, hầu hết các ứng dụng muốn sửa lỗi và phát triển hơn thì sử dụng TCP, nhưng một số ứng dụng cần tốc độ và giảm chi phí thì sử dụng UDP.

#### c, Tầng mạng (Network Layer)
Gần giống như tầng mạng của mô hình OSI. Tại đây, nó cũng được định nghĩa là một giao thức chịu trách nhiệm truyền tải dữ liệu một cách logic trong mạng. Các phân đoạn dữ liệu sẽ được đóng gói (Packets) với kích thước mỗi gói phù hợp với mạng chuyển mạch mà nó dùng để truyền dữ liệu. Lúc này, các gói tin được chèn thêm phần Header chứa thông tin của tầng mạng và tiếp tục được chuyển đến tầng tiếp theo. Các giao thức chính trong tầng là IP, ICMP và ARP.
  ![tcp ip](https://user-images.githubusercontent.com/97416839/148900091-cfc99224-bd40-4960-bd74-58e6f92edfc9.png)
#### d, Tầng vật lý (Physical Layer).
Là sự kết hợp giữa tầng Vật lý và tầng liên kết dữ liệu của mô hình OSI. Chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Tại đây, các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi đến đích đã được chỉ định ban đầu.
# 2. Sự tương quan giữa mô hình OSI và TCP/IP.
- Sự tương đồng giữa 2 mô hình:

    Cả 2 mô hình đều là mô hình triển khai giúp thiết lập kết nối giữa các thiết bị với nhau thông qua mạng Internet, chúng đều là mô hình logic và có kiến trúc tương tự nhau vì cả 2 được xây dựng dựa trên các lớp.
    
    Cả 2 cung cấp các tiêu chuẩn xác định và cung cấp khuân khổ được sử dụng để thực hiện các tiêu chuẩn và thiết bị.

 ![sự tương quan mô hình OSI và TCP](https://user-images.githubusercontent.com/97416839/148901118-fadafa1a-2a4b-468b-810b-89dda5a4f57a.png)

 Cấu trúc phân tầng tương ứng của 2 mô hình được thể hiện như hình trên trong đó:
 
 Tầng ứng dụng của mô hình TCP/IP bao gồm luôn cả 3 tầng trên của mô hình OSI.
 
 Tầng giao vận trong mô hình TCP/IP không phải luôn đảm bảo độ tin cậy của việc truyền dữ liệu như ở mô hình OSI mà cho phép có thêm 1 tùy chọn khác đó là UDP.
 
*Kết luận*

Mô hình TCP/IP đáng tin cậy đối với Mô hình OSI, TCP/IP được sử dụng cho kết nối đầu cuối để truyền dữ liệu qua internet. TCP/IP mạnh mẽ, linh hoạt, hữu hình và cũng gợi ý cách dữ liệu nên được gửi qua web. Lớp vận chuyển của Mô hình TCP/IP kiểm tra xem dữ liệu đã đến theo thứ tự chưa, nó có lỗi hay không, các gói bị mất có được gửi hay không, xác nhận có được nhận hay không, v.v.

