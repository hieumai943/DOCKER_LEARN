# 1. Docker  
## Docker là gì? 
**Docker** là một nền tảng để cung cấp cách để building, deploying và running ứng dụng dễ dàng hơn bằng cách sử dụng các containers (trên nền tảng ảo hóa). Ban đầu viết bằng Python, hiện tại đã chuyển sang Golang.  
## Container trong Docker là gì?
Các containers cho phép lập trình viên đóng gói một ứng dụng với tất cả các phần cần thiết, chẳng hạn như thư viện và các phụ thuộc khác, và gói tất cả ra dưới dạng một package.  
Bằng cách đó, nhờ vào container, ứng dụng sẽ chạy trên mọi máy Linux khác bất kể mọi cài đặt tùy chỉnh mà máy có thể có khác với máy được sử dụng để viết code.  
## Các khái niệm liên quan  
* **Docker Engine**: là thành phần chính của Docker, như một công cụ để đóng gói ứng dụng  
* **Docker Hub**: là một “github for docker images”. Trên DockerHub có hàng ngàn public images được tạo bởi cộng đồng cho phép bạn dễ dàng tìm thấy những image mà bạn cần. Và chỉ cần pull về và sử dụng với một số config mà bạn mong muốn.
* **Images**: là một khuôn mẫu để tạo một container. Thường thì image sẽ dựa trên 1 image có sẵn với những tùy chỉnh thêm. Ví dụ bạn build 1 image dựa trên image Centos mẫu có sẵn để chạy Nginx và những tùy chỉnh, cấu hình để ứng dụng web của bạn có thể chạy được. Bạn có thể tự build một image riêng cho mình hoặc sử dụng những image được chia sẽ từ cộng đồng Docker Hub. Một image sẽ được build dựa trên những chỉ dẫn của Dockerfile.  
* **Container**: là một instance của một image. Bạn có thể create, start, stop, move or delete container dựa trên Docker API hoặc Docker CLI.  
* **Docker Daemon**: lắng nghe các yêu cầu từ Docker Client để quản lý các đối tượng như Container, Image, Network và Volumes thông qua REST API. Các Docker Daemon cũng giao tiếp với nhau để quản lý các Docker Service.  
* **Dockerfile**: là một tập tin bao gồm các chỉ dẫn để build một image  
* **Volumes**: là phần dữ liệu được tạo ra khi container được khởi tạo.  
# 2. Docker-composer là gì?
## Docker Compose là một công cụ được sử dụng để định nghĩa và chạy nhiều ứng dụng Docker Container tại cùng một thời điểm. Với Docker Compose, bạn sử dụng tệp cấu hình YAML để định nghĩa các dịch vụ của ứng dụng  
## Sau khi định nghĩa, bạn có thể tạo và khởi động tất cả các dịch vụ từ file cấu hình của mình chỉ với một lệnh duy nhất. Docker Compose có thể xử lý đồng thời nhiều container trong sản xuất, staging, phát triển, thử nghiệm và CI( tích hợp liên tục).  
## Các bước sử dụng Docker Compose thường bao gồm:
* Khai báo môi trường ứng dụng trong Dockerfile.
* Khai báo các dịch vụ cần thiết để chạy ứng dụng trong file docker-compose.yml.
* Chạy lệnh docker-compose up để khởi động và chạy ứng dụng
# 3. Linux và Unix và BSD hay *nix? macOS thuộc loại nào?  
### Linux, Unix, BSD, và *nix đều là các hệ điều hành dựa trên Unix  
* Unix 
Unix ban đầu là một hệ điều hành của AT&T, nhưng ngày nay, nhãn hiệu UNIX thuộc về Open Group. Unix cũng được sử dụng để chỉ một nhóm hệ điều hành.
* Linux  
Linux là một thuật ngữ khác khó định nghĩa hơn nhiều. Về mặt kỹ thuật, một bản phân phối Linux hoàn chỉnh là một hệ điều hành “giống Unix”. Bản thân Linux chỉ là hạt nhân – phần của hệ điều hành thực hiện nhiệm vụ cốt lõi và giao tiếp với phần cứng.
* Giấy phép BSD  
BSD (Berkeley Software Distribution) ban đầu là những tập hợp sự thay đổi được Bell Unix tạo ra tại trường Đại học California, Berkeley. BSD và Linux là các hệ điều hành mã nguồn mở giống như Unix. Tuy nhiên, họ có các điều khoản cấp phép khác nhau: BSD sử dụng giấy phép BSD dễ dãi, trong khi Linux sử dụng Giấy phép Công cộng GNU (GPL) hạn chế hơn.
* nix là một thuật ngữ tổng quát để chỉ các hệ điều hành giống Unix, bao gồm Unix, Linux, và BSD.  
* Về macOS, đây là hệ điều hành dựa trên Unix, được phát triển và phân phối bởi Apple Inc5. Đây là hệ điều hành chính cho máy tính Mac5. macOS đã hỗ trợ tới ba loại kiến trúc khác nhau của các bộ vi xử lý, bắt đầu từ PowerPC năm 19995.
# 4. Alpine và Ubuntu?  
Alpine và Ubuntu là hai bản phân phối Linux phổ biến với các đặc điểm và ứng dụng riêng biệt.  
Alpine Linux nổi tiếng với kích thước nhỏ gọn và tiếp cận tối giản. Nó được thiết kế để nhẹ nhàng và tối ưu cho môi trường có tài nguyên hạn chế. Hình ảnh cơ sở Alpine đáng kể nhỏ hơn so với Ubuntu, làm cho nó lý tưởng cho môi trường container hóa nơi việc sử dụng tài nguyên hiệu quả là quan trọng. Alpine Linux sử dụng trình quản lý gói của riêng mình gọi là apk.  
Ubuntu  
Ubuntu là một bản phân phối phong phú hơn với dấu chân lớn hơn, cung cấp một loạt các gói và công cụ sẵn có. Ubuntu sử dụng Công cụ Gói Nâng cao (APT) làm hệ thống quản lý gói của mình.  
Cả hai đều tuyệt vời và mỗi hệ điều hành có ưu và nhược điểm của riêng mình. Alpine Linux thích hợp cho môi trường nhẹ nhàng và có tài nguyên hạn chế. Ubuntu, với dấu chân lớn hơn và lựa chọn gói rộng hơn, phù hợp cho nhiều ứng dụng. Nó có thể được sử dụng cho sử dụng máy tính để bàn, triển khai máy chủ và môi trường phát triển yêu cầu một bộ công cụ và thư viện phong phú
# 5. VNC  
VNC, viết tắt của “Virtual Network Computing”, là một công nghệ cho phép bạn điều khiển và truy cập vào một máy tính từ xa thông qua internet. Với VNC, bạn có thể quản lý, điều khiển và làm việc trên máy tính từ xa một cách thuận tiện và dễ dàng.  
VNC hoạt động dựa trên mô hình client/server. Máy tính cần được cài đặt thành một máy chủ VNC, trong khi máy tính khác muốn điều khiển từ xa cần cài đặt một trình xem VNC, hoặc còn gọi là client. Khi hai thành phần này được kết nối, máy chủ VNC sẽ chuyển gửi hình ảnh màn hình từ xa đến trình xem VNC.  
Ngoài việc xem màn hình từ xa, VNC cũng cho phép người dùng điều khiển máy tính từ xa bằng cách sử dụng bàn phím và chuột của thiết bị điều khiển. Điều này mang lại khả năng kiểm soát đầy đủ các hoạt động trên máy tính từ xa sau khi được cấp phép từ máy tính đó.
