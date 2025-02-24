# OpenSearch Autoscaling Operator for Kubernetes

## Tổng quan dự án
Một Kubernetes operator tùy chỉnh được phát triển để tự động điều chỉnh quy mô cụm OpenSearch dựa trên các chỉ số sử dụng và lịch trình được định nghĩa trước. Operator này giúp tối ưu hóa hiệu suất và chi phí bằng cách tự động mở rộng/thu hẹp số lượng node dữ liệu OpenSearch.

## Các tính năng chính
- **Tự động điều chỉnh quy mô thông minh**: Tự động điều chỉnh số lượng node dữ liệu dựa trên mức sử dụng CPU và bộ nhớ
- **Lập lịch linh hoạt**: Hỗ trợ lập lịch tăng/giảm quy mô theo thời gian với cú pháp cron
- **Cơ chế ổn định**: Cửa sổ ổn định có thể cấu hình để tránh thay đổi quy mô quá thường xuyên
- **Giám sát và Metrics**: Tích hợp với hệ thống metrics để theo dõi hiệu suất và quyết định điều chỉnh quy mô
- **Hỗ trợ nhiều môi trường**: Có thể triển khai trên cả AWS OpenSearch và OpenSearch tự host trên Kubernetes

## Kiến trúc kỹ thuật

### Thành phần chính

1. **OpenSearch Controller**
   - Xử lý reconciliation loop chính
   - Quản lý vòng đời của các tài nguyên OpenSearch
   - Thực hiện các quyết định điều chỉnh quy mô

2. **Evaluator**
   - Tính toán số lượng node mong muốn dựa trên metrics
   - Áp dụng các ràng buộc và quy tắc điều chỉnh quy mô
   - Xử lý cửa sổ ổn định

3. **Metrics Client**
   - Thu thập metrics sử dụng
   - Đẩy metrics về trạng thái hệ thống
   - Hỗ trợ ra quyết định điều chỉnh quy mô

### Quy trình hoạt động
1. Controller theo dõi các tài nguyên OpenSearch
2. Thu thập metrics về mức sử dụng
3. Evaluator tính toán số lượng node mong muốn
4. Áp dụng các ràng buộc và cửa sổ ổn định
5. Thực hiện điều chỉnh quy mô thông qua API

### Công nghệ sử dụng
- **Go**: Ngôn ngữ lập trình chính
- **Kubernetes**: Nền tảng container orchestration
- **OpenSearch**: Distributed search engine
- **controller-runtime**: Framework phát triển Kubernetes operators
- **AWS SDK**: Tương tác với AWS OpenSearch Service
- **Prometheus**: Thu thập và lưu trữ metrics

## Kết quả và tác động
- Giảm chi phí vận hành bằng cách tự động điều chỉnh tài nguyên
- Cải thiện hiệu suất hệ thống thông qua việc điều chỉnh quy mô chủ động
- Giảm thời gian quản trị thủ công
- Tăng độ tin cậy với cơ chế ổn định và giám sát

## Bài học kinh nghiệm

### Thiết kế hệ thống
- Tầm quan trọng của cơ chế ổn định để tránh thay đổi quá thường xuyên
- Cần cân nhắc kỹ các ngưỡng và quy tắc điều chỉnh quy mô

### Kỹ thuật
- Sử dụng controller-runtime hiệu quả cho Kubernetes operators
- Xử lý các edge case trong quá trình điều chỉnh quy mô
- Quản lý state và reconciliation loop

### Vận hành
- Tầm quan trọng của logging và monitoring
- Cần có chiến lược rollback cho các thay đổi quy mô
- Đảm bảo tính nhất quán của cluster trong quá trình scale

## Mã nguồn và tài liệu
[Liên kết đến mã nguồn và tài liệu chi tiết]

Bạn có thể điều chỉnh và bổ sung thêm các phần cụ thể dựa trên kinh nghiệm thực tế của mình với dự án này.
