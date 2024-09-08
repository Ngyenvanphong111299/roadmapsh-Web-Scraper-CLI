REQUIREMENTS
20. Web Scraper CLI
Difficulty: Very Difficult
Skills and technologies used: Web scraping, headless browsing, rules engine
A web scraper is a tool that allows you to navigate a website through code, and in the process, capture information from the presented web pages.
As part of the last backend project of this list, you’ll be implementing your very own web scraper CLI tool. This tool will take input from the user with a list of preset commands, such as:
show code: to list the HTML code of the current page.
navigate: to open a new URL
capture: this will return a subsection of the HTML of the current page using the CSS selector you specify.
click on: this command will trigger a click on a particular HTML element using a CSS selector provided.
Feel free to add extra commands to make the navigation even more interactive.
With the last of our backend project ideas, you’ve covered all the major areas involved in backend development and you’re more than ready to apply for a backend development job if you haven’t already.
If you find a piece of technology that wasn’t covered here, you’ll have the skills required to pick it up in no time.

STEPS:
1. Yêu cầu và phạm vi
Yêu cầu: Công cụ CLI có các tính năng:
show code: Liệt kê mã HTML của trang hiện tại.
navigate: Điều hướng đến URL mới.
capture: Trích xuất phần HTML theo CSS selector.
click on: Giả lập nhấn chuột vào phần tử HTML bằng CSS selector.
Phạm vi: Tập trung vào xây dựng công cụ CLI với .NET, tương tác với web qua HTTP requests và HTML parsing.

2. Công nghệ và thư viện
- Language/Frameworks: C#/.NET Core.
- Libraries:
	+ HttpClient: HTTP request and web content loading.
	+ HtmlAgilityPack: parsing HTML syntax.
	+ Selenium.WebDriver: interact with HTML elements (click, form filling, etc...).
- Project Architect: Modular Archirtect.

3. Thiết kế kiến trúc
CLI Tool: Sử dụng System.CommandLine hoặc McMaster.Extensions.CommandLineUtils để xây dựng giao diện dòng lệnh (CLI).
Các mô-đun chính:
HttpHandler: Xử lý yêu cầu HTTP và tải nội dung trang web.
HtmlParser: Sử dụng HtmlAgilityPack để phân tích và trích xuất nội dung HTML.
CommandProcessor: Xử lý các lệnh như navigate, show code, capture, click on.

4. Các tính năng chính
Xử lý lệnh CLI: Xây dựng giao diện CLI để người dùng nhập các lệnh (sử dụng System.CommandLine).
Chức năng navigate: Sử dụng HttpClient để gửi yêu cầu HTTP đến URL và lưu mã HTML của trang hiện tại.
Chức năng show code: In ra toàn bộ mã HTML của trang hiện tại bằng cách đọc kết quả từ HttpClient.
Chức năng capture: Sử dụng HtmlAgilityPack để trích xuất phần tử HTML dựa trên CSS selector do người dùng cung cấp.
Chức năng click on: Sử dụng Selenium.WebDriver để giả lập hành động nhấn chuột vào phần tử HTML xác định.

5. Kiểm thử và đảm bảo chất lượng
Kiểm thử các lệnh: Viết các unit test và kiểm tra tính năng từng lệnh (navigate, show code, capture, click on) để đảm bảo đúng yêu cầu.
Xử lý lỗi: Thêm các phương án xử lý lỗi như:
Trang web không phản hồi hoặc trả về lỗi.
CSS selector không hợp lệ hoặc không tìm thấy phần tử.

6. Bổ sung tính năng nâng cao
Thêm lệnh back: Quay lại trang trước trong lịch sử duyệt web.
Thêm lệnh input: Giả lập điền dữ liệu vào trường nhập liệu trên trang web.
Thêm lệnh download: Tải file hoặc nội dung từ trang web.
Logging: Tích hợp Serilog hoặc NLog để ghi lại log các thao tác và lỗi phát sinh.

7. Tối ưu hóa và cải tiến
Tối ưu hiệu suất: Đảm bảo quá trình tải và xử lý trang web diễn ra nhanh chóng, hạn chế độ trễ.
Cải thiện trải nghiệm người dùng: Cung cấp thông tin hướng dẫn và mô tả chi tiết cho từng lệnh trong CLI (có thể dùng --help).

8. Tài liệu và hướng dẫn sử dụng
Tạo tài liệu hướng dẫn: Viết chi tiết hướng dẫn sử dụng công cụ, bao gồm các ví dụ và mô tả các lệnh.
Ví dụ: Đưa ra các ví dụ về cách sử dụng từng lệnh như navigate, capture, và click on.

9. Đóng gói và phân phối
Đóng gói: Sử dụng dotnet pack để đóng gói dự án thành một gói có thể cài đặt và sử dụng dễ dàng.
Phân phối: Đăng tải công cụ lên GitHub hoặc NuGet để người dùng có thể cài đặt và sử dụng.

10. Triển khai và bảo trì
Triển khai: Phát hành phiên bản đầu tiên của công cụ và cung cấp hướng dẫn cài đặt.
Bảo trì: Tiếp tục cập nhật và cải tiến dựa trên phản hồi của người dùng, sửa lỗi và tối ưu thêm các tính năng.