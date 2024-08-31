+++
title = "Automate Load to S3"
date = 2024
weight = 1
chapter = false
+++

# Tải dữ liệu tự động lên S3 sử dụng airflow va thư viện boto3

#### Tổng quan

Ở bài thực hành này ta sẽ tìm hiểu cách automate load data to S3 một cách đơn giản. Automate load là một bước trong quy trình ETL mà cá data engineer thường làm. Vì vậy ở đây em sẽ load dữ liệu lên S3 một cách đơn giản nhất.


#### Amazon S3
**S3** (*Amazon Simple Storage Service*): Là dịch vụ đám mây lưu trữ do đó bạn có thể tải lên các tệp, các tài liệu, các dữ liệu tải về của người dùng hoặc các bản sao lưu.

#### Docker
**Docker**: Docker là một nền tảng cho developers và sysadmin để develop, deploy và run application với container. Nó cho phép tạo các môi trường độc lập và tách biệt để khởi chạy và phát triển ứng dụng và môi trường này được gọi là container. Ở bài học này ta sẽ sử dụng docker để kéo Image Aiflow từ Docker hub về. Sau đó chạy container với image airflow này để chạy Airflow trên môi trường localhost.

#### Airflow
**Airflow** : Airflow là một công cụ lập lịch trình cho luồng công việc của bạn cũng như hỗ trợ quản lý, theo dõi từng phần trong quy trình giúp bạn sửa lỗi, bảo trì code thuận tiện và dễ dàng. Trong bài học này, tôi sẽ sử dụng file có sẵn là imdb_top1000.zip tôi lấy từ kaggle để đưa lên S3. Sẽ không có bước ingest data theo từng ngày nên Airflow ở đây tôi dùng chỉ mang tính là cái tool chạy tự động để load lên S3 cho ngày hôm nay.

#### boto3
**Boto3**: Boto3 là một thư viện Python mạnh mẽ được phát triển bởi Amazon Web Services (AWS) để tương tác với các dịch vụ của AWS. Trong trường hợp này, chúng ta sẽ tập trung vào việc sử dụng Boto3 để làm việc với dịch vụ lưu trữ đám mây của AWS  S3.


  ![Diagram](../../../images/0/Load_to_s3.png?width=50pc)

#### Nội dung:
1. [Khởi tạo S3](1-s3)
2. [Tải môi trường cần thiết](2-environ)
3. [Cấu hình các file](3-config)
4. [Kiểm tra kết quả](4-result)
5. [Dọn dẹp tài nguyên](5-clean)