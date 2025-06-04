# Chu kỳ phản hồi yêu cầu là quy trình cơ bản mà máy khách, thường là trình duyệt web, giao tiếp với máy chủ để yêu cầu và nhận tài nguyên.

Các thành phần chính của chu kỳ phản hồi yêu cầu bao gồm máy khách, máy chủ và giao thức.
Máy khách là thực thể thực hiện yêu cầu.

Ví dụ.

Trình duyệt web hoặc máy chủ ứng dụng di động là thực thể phản hồi yêu cầu bằng tài nguyên được yêu cầu hoặc thông báo lỗi.
Và cuối cùng là giao thức.
Đó là tập hợp các quy tắc chi phối giao tiếp, ví dụ HTTP hoặc Https.
Bây giờ chúng ta hãy tìm hiểu các bước liên quan đến chu kỳ phản hồi yêu cầu.
Bước một, máy khách gửi yêu cầu.
Đây là khởi tạo.
Chu kỳ bắt đầu khi máy khách thực hiện yêu cầu truy cập tài nguyên, chẳng hạn như nhập URL vào trình duyệt web hoặc nhấp vào liên kết.
Vì vậy, yêu cầu này là tin nhắn yêu cầu.
Máy khách gửi tin nhắn yêu cầu HTTP đến máy chủ và tin nhắn này bao gồm dòng yêu cầu chứa phương thức.
Ví dụ, get, post, put, patch hoặc delete và chúng ta cũng sẽ xem xét chi tiết các phương thức này khi chúng ta tiến lên phía trước.
Vì vậy, dòng yêu cầu này cùng với phương thức cũng chứa đường dẫn tài nguyên và phiên bản HTTP HTTP 1.1 HTTP two.
Đây là các phiên bản HTTP khác nhau mà máy khách và máy chủ sử dụng để giao tiếp với nhau.

Tin nhắn yêu cầu(request message) cũng chứa tiêu đề(headers).
Tiêu đề(headers) cung cấp thông tin bổ sung về yêu cầu.
Ví dụ, tác nhân người dùng chấp nhận ngôn ngữ, cookie và nhiều đối tượng dữ liệu thông tin khác.
Và cuối cùng, chúng ta có phần thân yêu cầu(request body) chứa dữ liệu cho các phương thức như Post và phần này là tùy chọn.

Vì vậy, yêu cầu có thể chứa phần thân(body) hoặc không.
Tùy thuộc vào việc có điều gì đó bắt buộc trong phần thân hay có thể để trống phần thân(body).

### Bước tiếp theo trong chu kỳ phản hồi yêu cầu là phân giải DNS.
Vì vậy, chúng ta đã xem xét.
Tên miền này được chuyển đổi thành IP.
Máy khách cần biết địa chỉ IP của máy chủ để gửi yêu cầu.
Và nó sử dụng hệ thống Tên miền để phân giải tên miền thành địa chỉ IP.
Sau đó, trong quá trình tra cứu DNS, máy khách sẽ truy vấn máy chủ DNS trả về địa chỉ IP được liên kết với tên miền.
Ở bước tiếp theo, chúng ta thiết lập kết nối.
Máy khách thiết lập kết nối TCP với máy chủ thông qua quy trình bắt tay ba chiều.
Chúng ta cũng đã đề cập đến điều đó.
Và sau khi bắt tay TCP hoàn tất, nếu chúng ta sử dụng Https và SSL, bắt tay TLS sẽ diễn ra để thiết lập kết nối an toàn.

Ở bước tiếp theo, máy chủ sẽ nhận được yêu cầu.
Bây giờ, sau khi máy chủ nhận được thông báo yêu cầu của máy khách, máy chủ sẽ xử lý thông báo đó.
Và điều này liên quan đến việc phân tích cú pháp, nghĩa là diễn giải tiêu đề và nội dung của dòng yêu cầu.
Tiếp theo, định tuyến sẽ xác định trình xử lý phù hợp cho yêu cầu dựa trên đường dẫn tài nguyên và máy chủ cũng sẽ xác minh danh tính và quyền của Máy khách nếu cần.
Vì vậy, các trình xử lý mà chúng ta đang nói đến về cơ bản là các hàm.
Khi chúng ta truy cập một tuyến đường cụ thể, một hàm sẽ chạy trên máy chủ.
Và hàm đó sẽ trả về một số giá trị.
Và sau đó các giá trị đó được chuyển cho máy khách.
Chúng ta sẽ xem xét chi tiết điều này trong phần thực hành khi chúng ta thực hành tạo máy chủ, máy khách và API.

Bây giờ, sau khi yêu cầu được xử lý, bước tiếp theo là gửi phản hồi.
Máy chủ chuẩn bị phản hồi HTTP bao gồm dòng trạng thái cho biết kết quả của yêu cầu.
Ví dụ: 200, nghĩa là ổn hoặc 404 nghĩa là không tìm thấy.
Phản hồi cũng bao gồm tiêu đề.
Ví dụ: tiêu đề cung cấp siêu dữ liệu về phản hồi.
Kiểu nội dung.
Độ dài nội dung, nén và có rất nhiều tiêu đề mà chúng ta đưa vào phản hồi.
Và cuối cùng, phản hồi chứa nội dung.
Nội dung chứa tài nguyên được yêu cầu hoặc thông báo lỗi.
Bây giờ, sau khi phản hồi này được chuẩn bị, máy chủ sẽ gửi tin nhắn phản hồi trở lại máy khách qua kết nối đã thiết lập.
Bây giờ, sau khi máy chủ đã chuẩn bị phản hồi, máy chủ sẽ gửi tin nhắn phản hồi trở lại máy khách qua kết nối đã thiết lập.
Và ở bước cuối cùng, máy khách nhận được phản hồi.
Nó xử lý phản hồi và quá trình xử lý bao gồm việc phân tích cú pháp phản hồi, diễn giải tiêu đề và nội dung dòng trạng thái, cookie đã được máy chủ gửi cùng với phản hồi và sau đó hiển thị.
Nếu phản hồi chứa HTML, trình duyệt sẽ hiển thị trang web.
Nếu nó chứa dữ liệu, ví dụ JSON, thì máy khách sẽ xử lý dữ liệu theo đó.
Bởi vì khi chúng ta nhận được JSON, chúng ta không hiển thị bất kỳ thứ gì.
Chúng ta đang xử lý dữ liệu và sau đó xử lý dữ liệu theo cách phù hợp để trình bày dữ liệu cho máy khách cho người dùng.
Và cuối cùng, sau khi hiển thị hoặc xử lý dữ liệu, máy khách sẽ đóng kết nối.
Vì vậy, kết nối sẽ bị đóng hoặc được giữ nguyên cho các yêu cầu tiếp theo tùy thuộc vào tiêu đề kết nối.
Nếu tiêu đề kết nối cho phép duy trì kết nối, thì nó sẽ được duy trì.

### Bây giờ chúng ta hãy đến với một số khái niệm chính trong chu trình phản hồi yêu cầu.
Đầu tiên, chúng ta hãy thảo luận về các phương thức HTTP.
Đầu tiên là phương thức phổ biến nhất và được sử dụng thường xuyên nhất là get.
Yêu cầu Get nhận dữ liệu từ máy chủ.
Nó lấy dữ liệu từ máy chủ.
Yêu cầu Post Phương thức http post gửi dữ liệu đến máy chủ.
Chúng ta đang đăng một cái gì đó lên máy chủ và get có nghĩa là chúng ta đang nhận được một cái gì đó từ máy chủ.
Put có nghĩa là chúng ta đang cập nhật dữ liệu trên máy chủ và patch cũng giống vậy.
Put và patch giống nhau.

Chúng ta đang cập nhật dữ liệu trên máy chủ.
Tuy nhiên, put có nghĩa là chúng ta đang thay thế hoàn toàn một phần dữ liệu nhất định trên máy chủ và patch có nghĩa là chúng ta đang sửa đổi một phần tử nhất định, một phần dữ liệu nhất định.
Chúng ta không thay thế hoàn toàn dữ liệu, mà chỉ sửa đổi một chút.
Và cuối cùng chúng ta có phương thức delete, được sử dụng để xóa dữ liệu khỏi máy chủ.

Tiếp theo chúng ta có mã trạng thái.
Mã trạng thái bắt đầu bằng hai mã trạng thái thành công R.
Yêu cầu đã được nhận, hiểu và chấp nhận thành công.
Ví dụ 200 được rồi, tiếp theo chúng ta có mã trạng thái bắt đầu bằng ba như 301.
Vì vậy, đây là mã trạng thái chuyển hướng.
Các mã trạng thái này có nghĩa là cần thực hiện thêm hành động để hoàn tất yêu cầu.
Vì vậy, 301 là một ví dụ có nghĩa là đã di chuyển vĩnh viễn.
Nhưng có nhiều mã trạng thái khác bắt đầu bằng ba.
Vì vậy, đó là chuỗi 300 có nghĩa là cần thực hiện thêm hành động để hoàn tất yêu cầu.
Tiếp theo, chúng ta đến chuỗi 400.
Nó có nghĩa là lỗi của máy khách.
Yêu cầu chứa cú pháp sai hoặc không thể thực hiện được.

Vì vậy, tất cả các mã phản hồi 400 có nghĩa là có một số vấn đề về cú pháp hoặc có một số vấn đề với yêu cầu mà máy chủ không thể thực hiện được.

Ví dụ tốt nhất là mã 404.
Mã trạng thái 404, nghĩa là không tìm thấy tài nguyên và chuỗi cuối cùng là chuỗi 500, nghĩa là lỗi máy chủ.

Vì vậy, máy chủ đã không thực hiện được yêu cầu hợp lệ.
Nếu điều đó xảy ra, chúng ta sẽ sử dụng mã trạng thái chuỗi 500.
Một ví dụ hay và được sử dụng thường xuyên nhất là mã trạng thái 500, nghĩa là lỗi máy chủ nội bộ
Bây giờ, một khái niệm khác liên quan đến chu kỳ phản hồi yêu cầu là tiêu đề.
Chúng ta có tiêu đề trong yêu cầu cũng như phản hồi.
Tiêu đề yêu cầu cung cấp thông tin bổ sung về máy khách và yêu cầu.

Ví dụ, nó bao gồm cặp giá trị khóa như chấp nhận văn bản HTML.
Tiếp theo, chúng ta có tiêu đề phản hồi và tiêu đề phản hồi.
Cung cấp thông tin bổ sung về máy chủ và phản hồi.
Ví dụ: ứng dụng JSON Content-Type.
Vì vậy, nội dung mà chúng ta đang gửi đến máy khách từ máy chủ có kiểu JSON.
Và chúng ta sẽ thấy tất cả những điều này hoạt động khi chúng ta bắt đầu tạo API của riêng mình.
Khi chúng ta bắt đầu làm việc, khi chúng ta bắt đầu thực hành tạo máy chủ và máy khách.
Bây giờ chúng ta hãy đến với một số trường hợp sử dụng thực tế và ví dụ về chu kỳ phản hồi yêu cầu.
Một trường hợp sử dụng thực tế đơn giản là truy cập vào một trang web.
Khi bạn nhập example.com trong trình duyệt của mình, một yêu cầu Get sẽ được gửi đến máy chủ lưu trữ example.com.
Máy chủ phản hồi bằng một tài liệu HTML mà trình duyệt hiển thị dưới dạng trang web.
Trường hợp sử dụng tiếp theo là để gửi biểu mẫu khi bạn gửi biểu mẫu trên một trang web.
Một yêu cầu đăng được gửi đến máy chủ có dữ liệu biểu mẫu trong phần nội dung.
Máy chủ xử lý dữ liệu và phản hồi bằng thông báo thành công hoặc lỗi.

Trường hợp sử dụng tiếp theo là các lệnh gọi API.
Khi một ứng dụng thực hiện lệnh gọi API đến, chẳng hạn như https colon backslash backslash API dot example.com slash data hoặc yêu cầu get sẽ được gửi đến máy chủ API.
Sau đó, máy chủ phản hồi bằng dữ liệu JSON, ứng dụng sẽ xử lý và hiển thị dữ liệu này cho người dùng.
Một số phương pháp hay nhất liên quan đến chu kỳ phản hồi yêu cầu là.
Vâng, chúng ta nên giảm thiểu số lượng yêu cầu bằng cách kết hợp các tài nguyên.

Ví dụ CSS, JavaScript.
Và chúng ta cũng có thể tối ưu hóa các yêu cầu bằng cách sử dụng bộ nhớ đệm.
Tiếp theo, chúng ta nên xử lý lỗi một cách khéo léo bằng cách triển khai xử lý lỗi phù hợp và hiển thị thông báo lỗi thân thiện với người dùng.
Và cuối cùng, chúng ta nên sử dụng Https để mã hóa dữ liệu được truyền giữa máy khách và máy chủ.
Chu kỳ phản hồi yêu cầu là một quy trình cơ bản trong giao tiếp web bao gồm nhiều bước từ yêu cầu của máy khách đến phản hồi của máy chủ.
Việc hiểu chu kỳ này rất quan trọng để chẩn đoán và khắc phục sự cố liên quan đến web.
Trong bài giảng toàn diện này, chúng tôi đã trình bày quy trình cơ bản của chu kỳ phản hồi yêu cầu trong giao tiếp web, giải thích chi tiết từng bước liên quan mà không đi sâu vào lập trình hoặc mã.

Chúng tôi đã thảo luận về các khái niệm quan trọng, các vấn đề phổ biến và các phương pháp hay nhất để tối ưu hóa và bảo mật giao tiếp web.

![App Screenshot](https://github.com/WP-Tien/Internet/blob/master/request_reponse_cycle/img1.png)

![App Screenshot](https://github.com/WP-Tien/Internet/blob/master/request_reponse_cycle/img2.png)