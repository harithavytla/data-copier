# data-copier
Copies data from MySQL to Postgres.

Refer to the readme of https://github.com/harithavytla/retail-data-pipeline-ETL.git repository for the required setup. 

*** Run Application ***

This can be done using Pycharm or Docker. Below are the steps for docker.

1.Building Docker Image - 
```
docker build -t data-copier
```
2.Running Application using Docker with entrypoint.
```
docker run --name data-copier \
  -v `pwd`:/app \
  -it \
-e SOURCE_DB_USER=retail_user \
-e SOURCE_DB_PASS='' \
-e TARGET_DB_USER=retail_user \
-e TARGET_DB_PASS='' \
--entrypoint python \
data-copier app.py dev all
```
