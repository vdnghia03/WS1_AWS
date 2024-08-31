+++
title = "Cấu trúc thư mục"
date = 2024
weight = 3
chapter = false
pre = "<b>2.3 </b>"
+++

1. Thư mục trong pycharm mình tổ chức như trong ảnh
   - Folder
   ![Create bucket](../../../images/2/2.3.infi.png)
   - Render
   ![Create bucket](../../../images/2/2.3.1.png)

2. Hiểu sơ qua về các thư mục
   - `Dags`: Đây là thư mục ánh xạ tới ổ đĩa */opt/airflow/Dags* trong Docker Desktop của ta. Đây là nơi chuyển các dòng code ta viết trên local và đưa lên airflow
   - `Download`: Đây là thư mục ánh xạ tới ổ đĩa */opt/airflow/Download* trong Docker Desktop của ta. Ở đây Download là thư mục mà có tác dụng là kéo dữ liệu về từ các Resource khác và lưu ở đây. 
   - `Scripts`: Đây là thư mục ánh xạ tới ổ đĩa /opt/airflow/Scripts trong Docker Desktop của ta. Thực hiện tác vụ Load lên S3 bằng code python
   - `Docker-compose.yml`: Kéo image từ docker hub về.


