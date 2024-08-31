+++
title = "Cau hình Docker-compose.yml"
date = 2024
weight = 4
chapter = false
pre = "<b>3.4 </b>"
+++


1. Quan trọng nhất, ta chạy trong localhost nên cần phải có docker. Trong tương lai ta sẽ set up mọi thứ lên EC2 chạy airflow và các dòng code lên đưa lên tu local bằng putty luôn. Còn giờ ta chưa thành thạo nên làm airflow trên docker trước.

```
    version: '3.0'

    services:

    Load_s3_use_airflow:
        image: apache/airflow:2.3.0-python3.8
        volumes:
        - ./dags:/opt/airflow/dags
        - ./download:/opt/airflow/download
        - ./scripts:/opt/airflow/scripts


        ports:
        - 8080:8080

        command: bash -c '(airflow db init && airflow users create --username admin --password admin --firstname nghia --lastname vd --role Admin --email voduyanqn1972@gmail.com); airflow webserver & airflow scheduler'

    volumes:
    dags:
    download:
    scripts:


```

{{% notice tip %}}
Để ý ta thấy trong volumn set up ta đưa vào các thư mục ta đã tạo như dags, download, scripts.
Ở comand bạn đổi là email name password của thì vẫn được nha.
{{% /notice%}}