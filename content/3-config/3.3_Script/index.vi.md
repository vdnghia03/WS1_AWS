+++
title = "Tạo file python dùng thư viện boto3"
date = 2024
weight = 3
chapter = false
pre = "<b>3.3 </b>"
+++


1. Viết code vào file upload_s3.py của mục scripts
```
    import boto3
    import os

    airflow_home = os.environ['AIRFLOW_HOME']

    access_key = 'your access key created'
    secret_key = 'your secret access key'


    filepath = f'{airflow_home}/download/imdb_top1000.zip'


    s3_bucket_name = 'nghiavd-aws-bucket'
    s3_file_name = 'imdb_top1000.zip'

    client = boto3.client(
        's3',
        aws_access_key_id=access_key,
        aws_secret_access_key=secret_key
    )

    # Upload file lên S3
    client.upload_file(filepath, s3_bucket_name, s3_file_name)

```

{{% notice info %}}
access_key và secret_key có giá trị của trong files csv mình lưu lại ở bước tạo access key. Bạn lấy hai dãy đó thế vào là được.
{{% /notice%}}


{{% notice warning %}}
Các đường dẫn có được như f'{airflow_home}/download/imdb_top1000.zip' là theo đường dẫn của docker. Nếu bạn thay đổi thì tìm hiểu thêm, còn không thì làm giống mình để không bị lỗi.
{{% /notice%}}
