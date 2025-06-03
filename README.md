# How internet Work

- Clients and Servers
- Protocols
- IP Addresses
- Domain Name System (DNS)

Vì vậy, mục tiêu của phần này là hiểu cách thức hoạt động của Internet, quá trình truy cập trang web và những gì xảy ra khi bạn nhập địa chỉ trang web và nhấn Enter.
Internet là mạng lưới toàn cầu gồm các máy tính được kết nối với nhau, giao tiếp bằng các giao thức chuẩn hóa và các thành phần chính là máy khách và máy chủ.
(So the internet is a global network of interconnected computers that communicate using standardized protocols, and the key components are clients and servers.)

Các máy khách yêu cầu tài nguyên và máy chủ cung cấp tài nguyên.
Vì vậy, máy khách có thể là trình duyệt hoặc ứng dụng, ứng dụng và điện thoại di động của chúng ta. Và máy chủ là máy chủ đang gửi dữ liệu mà chúng ta yêu cầu. Vì vậy, người dùng cuối là máy khách và chủ yếu là trình duyệt, còn máy chủ là công ty sở hữu ứng dụng sẽ cung cấp cho bạn dữ liệu mà bạn yêu cầu, bằng cách sử dụng trang web hoặc ứng dụng của họ. Hiện nay, có nhiều giao thức khác nhau liên quan trên internet và các giao thức này là các quy tắc xác định cách dữ liệu được truyền đi.

Ví dụ HTTP, https, TCP, IP và những thứ tương tự như vậy.
Vì vậy, chúng ta cũng sẽ xem xét chúng.
Và thành phần chính tiếp theo là địa chỉ IP.
Đây là các mã định danh duy nhất cho các thiết bị trên internet.

Và cuối cùng, chúng ta có Hệ thống tên miền DNS.
DNS dịch tên miền mà con người có thể đọc được thành địa chỉ IP.
Bây giờ, khi chúng ta mở một trang web trên trình duyệt của mình, hành trình của một yêu cầu web là gì?
Bước một là nhập URL.
Vì vậy, khi bạn nhập một URL như google.com hoặc gmail.com, hoặc bất kỳ example.com, bất kỳ tên miền nào trong trình duyệt của bạn và bạn nhấn enter, trình duyệt sẽ bắt đầu quá trình tải trang web.
Tiếp theo, ở bước hai, chúng ta có tra cứu DNS.
Trình duyệt kiểm tra bộ nhớ đệm của mình để xem liệu nó đã biết địa chỉ IP cho tên miền hay chưa.
Nếu chưa, nó sẽ truy vấn máy chủ DNS để lấy địa chỉ IP được liên kết với tên miền.
Và tiếp theo, chúng ta có tương tác với máy chủ DNS liên quan đến cùng một bước.
Vì vậy, trình duyệt gửi truy vấn DNS đến trình phân giải DNS.
Trình phân giải sẽ kiểm tra bộ nhớ đệm của mình nếu không tìm thấy địa chỉ IP.
Nó sẽ truy vấn các máy chủ DNS khác theo cách phân cấp.
Máy chủ DNS gốc chuyển hướng trình phân giải đến tên miền cấp cao nhất TLD, máy chủ DNS, máy chủ example.com hoặc các máy chủ tương tự.
Vì vậy, máy chủ DNS TLD chuyển hướng trình phân giải đến máy chủ DNS có thẩm quyền.
Sau đó là TLD.
Máy chủ DNS tên miền cấp cao nhất chuyển hướng trình phân giải đến máy chủ DNS có thẩm quyền cho Google.com hoặc bất kỳ tên miền nào bạn đã nhập.
Vì vậy, google.com hoặc Gmail hoặc bất kỳ trang web nào.
Com để nó truy vấn máy chủ DNS cấp cao nhất cho tên miền.
Tiếp theo, máy chủ DNS có thẩm quyền phản hồi bằng địa chỉ IP cho tên miền, đó là w-w-w dot
example.com.
Và sau đó, chúng tôi thiết lập kết nối TCP.
Vì vậy, bước thứ ba liên quan đến việc thiết lập kết nối TCP.
Trình duyệt sử dụng địa chỉ IP để thiết lập kết nối với máy chủ web lưu trữ trang web.
Điều này liên quan đến giao thức TCP IP.
Trình duyệt gửi một gói tin được đồng bộ hóa TCP đến máy chủ.
Máy chủ phản hồi lại bằng một gói tin đồng bộ hóa cũng như xác nhận, sau đó trình duyệt gửi một gói tin được xác nhận để hoàn tất quá trình bắt tay ba chiều.
Đây là quá trình bắt tay TCP.
Bước đầu tiên.
Trình duyệt gửi một gói tin được đồng bộ hóa.
Ở bước tiếp theo, máy chủ phản hồi không chỉ bằng gói tin được đồng bộ hóa mà còn bằng gói tin xác nhận.
Và sau đó, trình duyệt gửi một gói tin xác nhận trở lại máy chủ như một xác nhận.
Và đây là quá trình bắt tay ba chiều.
Và bây giờ ở bước bốn, chúng ta gửi một yêu cầu HTTP.
Trình duyệt gửi một yêu cầu HTTP đến máy chủ, chỉ định tài nguyên mà nó muốn truy xuất.
Shreve.
Ví dụ: yêu cầu get cho index dot HTML và yêu cầu có loại HTTP 1.1.
Nó tuân theo giao thức HTTP một.
Ở bước năm, máy chủ xử lý yêu cầu và truy xuất tài nguyên được yêu cầu và gửi phản hồi HTTP trở lại trình duyệt.
Phản hồi HTTP bao gồm mã trạng thái, ví dụ: mã trạng thái 200, có nghĩa là ổn, và một số tiêu đề như nén loại nội dung hoặc bất kỳ thông tin bổ sung nào và rất nhiều thông tin, rất quan trọng đối với yêu cầu và phản hồi.
Và nó cũng có thể chứa cookie.
Và cùng với tiêu đề và mã trạng thái, nó gửi tài nguyên được yêu cầu, ví dụ,
Nội dung HTML hoặc chỉ dữ liệu JSON, bao gồm dữ liệu được lấy từ cơ sở dữ liệu, ở định dạng bảng và được chuyển đổi thành định dạng chuỗi, định dạng chuỗi JSON để dễ dàng truyền qua internet.
Và cuối cùng, ở bước sáu, chúng ta sẽ hiển thị trang web hoặc chúng ta sẽ gửi dữ liệu được yêu cầu
dưới dạng dữ liệu JSON.
Vì vậy, trình duyệt nhận được phản hồi HTTP, phân tích cú pháp HTML và hiển thị trang web.
Quá trình hiển thị liên quan đến mô hình đối tượng tài liệu, vì vậy trình duyệt xây dựng Dom từ các phần tử HTML mà nó nhận được từ máy chủ.
Nó sẽ tìm nạp và xử lý các tài nguyên bổ sung, ví dụ như CSS, JavaScript và hình ảnh, sau đó trình duyệt sẽ hiển thị biểu diễn trực quan của trang web trên màn hình.
Vì vậy, một điều mà bạn có thể thắc mắc là quy trình bắt tay TCP.
Vì vậy, trước tiên chúng ta hãy tìm hiểu TCP là gì.
Bây giờ có các lớp mạng khác nhau liên quan khi chúng ta giao tiếp qua internet.
Vì vậy, lớp ứng dụng là các giao thức HTTP, Https và DNS.
Chúng chịu trách nhiệm cho các API cấp cao, chia sẻ tài nguyên và truy cập tệp từ xa.
Tiếp theo, chúng ta có lớp vận chuyển là TCP và UDP.
Lớp này chịu trách nhiệm cho giao tiếp đầu cuối.
Và tiếp theo, chúng ta có lớp internet.
Giao thức là IP và chịu trách nhiệm giải quyết định tuyến và chuyển tiếp gói tin.
Và cuối cùng, chúng ta có lớp liên kết.
Và trên lớp liên kết này, chúng ta có các giao thức như Ethernet và Wi-Fi.
Vì vậy, lớp này chịu trách nhiệm giải quyết địa chỉ vật lý và kiểm soát quyền truy cập phương tiện truyền thông địa chỉ Mac của thiết bị của bạn.
Bây giờ, chúng ta hãy đến với bắt tay TCP.
TCP sử dụng bắt tay ba chiều để thiết lập kết nối đáng tin cậy.
Và khi chúng ta có kết nối đáng tin cậy, chúng ta có thể gửi yêu cầu và nhận phản hồi từ máy chủ.
Vì vậy, kết nối là song công hoàn toàn.
Và cả hai bên đồng bộ hóa và xác nhận lẫn nhau.
Và chúng ta đã xem xét rằng trước tiên trình duyệt sẽ gửi một gói tin đã đồng bộ hóa.

Và sau đó máy chủ phản hồi bằng cách đồng bộ hóa cũng như gói xác nhận, sau đó máy khách gửi một gói xác nhận đến.

Hoàn tất bắt tay TCP.
Cho đến nay, chúng ta đã hiểu cách chúng ta truy cập vào một trang web.
Điều gì xảy ra khi chúng ta gửi yêu cầu đến trang web?
Khi chúng ta nhập tên miền vào thanh địa chỉ và nhấn enter.
Nhưng bây giờ chúng ta hãy đến với URL, địa chỉ web mà chúng ta đang nhập vào thanh địa chỉ.
Vậy URL hoạt động như thế nào và Internet hoạt động như thế nào cùng với URL.
Vậy URL hoặc URI, nó là viết tắt của Uniform Resource Locator trong khi bạn là I là viết tắt của Uniform Resource Identifier.
Về cơ bản, đây là các địa chỉ giúp chúng ta định vị các tài nguyên như trang web, hình ảnh, video, v.v. trên Internet.
Vì vậy, mỗi tài nguyên sẽ có một URL duy nhất hoặc một URI duy nhất.
Vì vậy, các thành phần của URL hoặc URI bao gồm giao thức.
Vì vậy, ban đầu chúng ta có giao thức chỉ định cách trình duyệt sẽ truy xuất tài nguyên.
Ví dụ: http, https và ftp.
HTTP và Https là Giao thức truyền siêu văn bản và Https có an toàn không?
Và chúng được sử dụng để truyền các trang web và nội dung khác giữa máy khách và máy chủ.
FTP có nghĩa là giao thức truyền tệp và được sử dụng để truyền tệp giữa các máy tính.
Và giao thức mà chúng ta đã thảo luận.
HTTP https và FTP.
Chúng cũng được gọi là lược đồ, vì vậy lược đồ và giao thức là một.
Tiếp theo chúng ta có máy chủ.
Máy chủ cũng là tên miền hoặc địa chỉ IP.
Tên miền phân giải thành địa chỉ IP và thực tế là máy chủ vì nó đang lưu trữ máy chủ
sẽ gửi cho bạn thông tin sẽ gửi cho bạn phản hồi.
Thành phần tiếp theo của URL là cổng.
Bây giờ cổng là tùy chọn.
Mặc định là 88 số không cho HTTP và 443 cho Https.
Vì vậy, bây giờ chúng ta có thể kết hợp nó để tạo thành HTTP.
Và sau đó là dấu hai chấm hai dấu gạch chéo về phía trước.
Và sau đó là w-w-w là World Wide Web dot Google, là máy chủ hoặc tên miền.com.
Và như chúng tôi đã nói, cổng là tùy chọn.
Vì vậy, chúng ta không cần cổng ở đây.
Nhưng khi chúng ta tạo API của riêng mình, thì trong trường hợp đó, chúng ta sẽ yêu cầu cổng phải chính xác và có thể truy cập API, máy chủ của chúng ta trong quá trình phát triển.
Khi chúng ta lưu trữ nó trên một địa chỉ IP, thì chúng ta sẽ không yêu cầu cổng.
Nhưng trong quá trình phát triển, chúng ta cần cổng để truy cập API hoặc máy chủ của mình.
Và bây giờ không phải tất cả vì đó là điều phổ biến nhất mà chúng ta làm.
Nhưng ngoài ra, còn có một số thứ khác cũng là thành phần của URL.
Ngoài ra, còn có những thứ khác cũng là thành phần của URL.
Vì vậy, tiếp theo chúng ta có đường dẫn.
Đường dẫn là đường dẫn tài nguyên cụ thể, vị trí cụ thể của tài nguyên trên máy chủ.
Ví dụ example.com slash images slash picture dot jpg.
Vậy đó là vị trí cụ thể của tài nguyên trên máy chủ.
Giống như chúng ta có đường dẫn cho một thư mục hoặc tệp trên hệ điều hành, chúng ta có đường dẫn cho một tài nguyên cụ thể trên máy chủ.
Và tiếp theo chúng ta có truy vấn các tham số truy vấn.
Vì vậy, truy vấn là một chuỗi các cặp giá trị khóa được sử dụng để truyền tham số.
Đây là tùy chọn.
Vì vậy, các tham số tùy chọn có thể được truyền đến máy chủ.
Và chúng được truyền đến máy chủ bằng dấu chấm hỏi.
Vì vậy, chúng ta sử dụng dấu chấm hỏi.
Và sau dấu chấm hỏi.
Theo sau dấu chấm hỏi, chúng ta sử dụng cặp giá trị khóa theo định dạng khóa bằng giá trị.
Ví dụ, hãy sử dụng w-w-w chấm example.com dấu chấm hỏi category bằng tech và chúng ta có thể sử dụng cả path cũng như query cùng nhau.
Vì vậy, nó có thể là w-w-w chấm example.com dấu gạch chéo hình ảnh dấu gạch chéo hình ảnh dấu chấm jpg dấu chấm hỏi category bằng tech.
Giao thức được sử dụng ở đây là https và tên miền là example.com.

Đường dẫn là hình ảnh gạch chéo hình ảnh chấm jpg và tham số truy vấn là dấu chấm hỏi danh mục bằng thẻ.
Vậy đây là URL hoàn chỉnh và tất cả các thành phần của URL.
Bây giờ chúng ta đã hiểu thêm một chút về URL.
Hãy đi sâu hơn một chút về URL và URI.
Trước đó, tôi đã sử dụng URI và URL thay thế cho nhau, nhưng có một chút khác biệt.
Vậy URI là Mã định danh tài nguyên thống nhất.
URI là chuỗi ký tự được sử dụng để xác định tài nguyên.
Nó có thể được phân loại thành URL, là Định vị tài nguyên thống nhất, chỉ định vị trí của tài nguyên và cũng có thể được phân loại thành Urn Tên tài nguyên thống nhất, xác định tài nguyên theo tên trong không gian tên.
Vậy thì URL là gì?
Vậy URL là một loại URI cụ thể cung cấp phương tiện để định vị tài nguyên trên internet.
Nó bao gồm đường dẫn miền giao thức và tùy chọn là chuỗi truy vấn và đoạn mã.
Vậy đó là URL.
Bây giờ bạn đã biết sự khác biệt giữa URL và URI.
Và bạn cũng biết một thuật ngữ kỹ thuật khác là u r n.
Vậy dữ liệu được truyền giữa máy chủ và máy khách như thế nào.
Vâng, dữ liệu được truyền bằng các gói dữ liệu.
Thông tin được gửi qua internet được chia thành các gói nhỏ.
Mỗi gói di chuyển độc lập đến đích, nơi chúng được lắp ráp lại.

Và chúng ta đã biết rằng chúng ta chuyển đổi tên miền như w-w-w dot example.com thành địa chỉ IP như 192.0.2.1 bằng cách sử dụng hệ thống Tên miền.
Vì vậy, những địa chỉ này được máy tính sử dụng để giao tiếp qua internet.
Vì vậy, mỗi IP là duy nhất.
Và do đó, chúng ta giao tiếp cụ thể với một máy chủ mục tiêu và một máy khách mục tiêu.
Bây giờ chúng ta hãy tìm hiểu mối quan hệ giữa URL và địa chỉ IP.
Khi bạn nhập URL vào trình duyệt web, trình duyệt cần tìm máy chủ tương ứng nơi lưu trữ trang web hoặc tài nguyên.
Trình duyệt thực hiện điều này bằng cách đầu tiên chuyển đổi tên miền như example.com thành địa chỉ IP, như 192.0.2.1 thông qua một quy trình được gọi là Phân giải Hệ thống Tên miền DNS.
Phân giải DNS có nghĩa là máy chủ DNS trên internet Duy trì cơ sở dữ liệu ánh xạ tên miền thành địa chỉ IP.
Khi bạn nhập URL, máy tính của bạn sẽ liên hệ với máy chủ DNS để lấy địa chỉ IP được liên kết với tên miền đó.
Khi có địa chỉ IP, máy tính có thể gửi yêu cầu đến máy chủ thích hợp để truy xuất trang web hoặc tài nguyên.
Bây giờ chúng ta hiểu rằng trong khi URL và địa chỉ IP có liên quan với nhau theo nghĩa là URL giúp định vị tài nguyên trên internet và dựa vào địa chỉ IP để giao tiếp thực tế, thì chúng phục vụ các mục đích khác nhau.
URL cung cấp một cách thuận tiện, dễ đọc đối với con người để truy cập tài nguyên, trong khi địa chỉ IP là mã định danh số được sử dụng để định tuyến dữ liệu qua các mạng.

Hoạt động.

Bây giờ chúng ta hiểu tại sao URL và địa chỉ IP của bạn có liên quan với nhau theo nghĩa là URL giúp định vị tài nguyên trên internet và dựa vào địa chỉ IP để giao tiếp thực tế.
Chúng phục vụ các mục đích khác nhau.
URL cung cấp một cách thuận tiện, dễ đọc đối với con người để truy cập tài nguyên, trong khi địa chỉ IP là mã định danh số được sử dụng để định tuyến dữ liệu qua các mạng.
Tóm lại, quá trình truy cập một trang web bao gồm nhiều bước như nhập URL, tra cứu DNS, thiết lập kết nối TCP, gửi yêu cầu HTTP, nhận phản hồi và hiển thị trang web.

Hiểu các bước này có thể giúp chẩn đoán và khắc phục sự cố liên quan đến quyền truy cập trang web.

![App Screenshot](https://github.com/WP-Tien/Internet/web_request.png)