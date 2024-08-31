+++
title = "Kiểm tra kết quả"
date = 2024
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

1. Chạy lệnh `docker compose up` trên cmd để build image.
![Create bucket](../../../images/4/4.0.png)
![Create bucket](../../../images/4/4.1.png)

{{% notice warning %}}
Phải bật docker desktop trước khi chạy lệnh `docker compose up`
{{% /notice%}}

2. Mở localhost cổng 8080 để chạy airflow
![Create bucket](../../../images/4/4.2.png)

![Create bucket](../../../images/4/4.3.png)

Hiện màu xanh đậm như thế là thành công.

3. Kiểm tra lại trên S3

![Create bucket](../../../images/4/4.4.png)

### Complete