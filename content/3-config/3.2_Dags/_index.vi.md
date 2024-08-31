+++
title = "Cấu hình airflow"
date = 2024
weight = 2
chapter = false
pre = "<b>3.2 </b>"
+++


1. Viết code vào file upload_to_s3.py

```
    from datetime import datetime
    from airflow import DAG

    from airflow.operators.bash import BashOperator
    from airflow.operators.python import PythonOperator


    import os
    airflow_home = os.environ['AIRFLOW_HOME']


    with DAG(
        dag_id='aws_workshop1'
        , start_date=datetime(2024, 8, 29)
        , schedule_interval='@daily'
    ) as dag:

        load_to_s3 = BashOperator(
            task_id='load_s3'
            , bash_command=f'python {airflow_home}/scripts/upload_s3.py'
        )


    load_to_s3

```
![Create bucket](../../../images/3/3.1.2.png)

{{% notice warning %}}
Các đường dẫn có được như f'python {airflow_home}/scripts/upload_s3.py' là theo đường dẫn của docker. Nếu bạn thay đổi thì tìm hiểu thêm, còn không thì làm giống mình để không bị lỗi.
{{% /notice%}}

1. Giải thích sơ qua về code
   - Step1: Import các thư viện
   - Step2: Lấy biến môi trường AIRFLOW_HOME:
   - Step3: Định nghĩa DAG:
   - Step4: Định nghĩa Task:
   - Step5: Chạy DAG:
  
Lên chat gpt hỏi thì sẽ giải thích cụ thể cho mình.

