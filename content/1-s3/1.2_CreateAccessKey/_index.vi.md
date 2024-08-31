+++
title = "Tạo access key"
date = 2024
weight = 2
chapter = false
pre = "<b>1.2 </b>"
+++

#### Tạo access key trong AMI

1. Chọn vào AMI
![Create bucket](../../../images/1/1.2.0.png)

2. Chọn vào user và admin user
![Create bucket](../../../images/1/1.2.1.png)

   - Admin User mình có được là từ lab0001 (https://000001.awsstudygroup.com/vi/). Và mình sử dụng Admin User để đăng nhập vào AWS thay vì dùng root user
  


3. Chọn **Security credentials** và sau đó chọn **create access key** để bắt đầu tạo access key

![Create bucket](../../../images/1/1.2.2.png)

4. Cấu hình access key
![Create bucket](../../../images/1/1.2.4.png)
![Create bucket](../../../images/1/1.1.5.png)
![Create bucket](../../../images/1/1.2.6.png)

- Ở trên một là bạn nhớ hai dãy số là `Access key` và `Secret access key`
- Hai là bạn download file csv bên dưới và lưu nó trong ổ đĩa của mình. Nó sẽ lưu cho bạn Access key và Secret access key

{{% notice warning %}}
Hãy chắc chắn rằng bạn đã lưu **access key** và **secret access key**. Đây là tham số quan trọng ta đưa vào code python sử dụng thư viện boto3 để kết nối đến aws S3
{{% /notice%}}

- Cuối cùng chọn Done, và như hình bên dưới thì bạn đã có được một access key
![Create bucket](../../../images/1/1.2.3.png)