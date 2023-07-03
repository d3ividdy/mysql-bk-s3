# mysql-bk-s3

Mysql Bakup Aws S3

## CLI

```sh
docker run --rm \
  --network host \
  -e MYSQL_HOST='host' \
  -e MYSQL_PORT='port' \
  -e MYSQL_USER='user' \
  -e MYSQL_PASS='pass' \
  -e MYSQLDUMP_DATABASE='database' \
  -e MYSQLDUMP_OPTIONS='more options' \
  -e S3_ACCESS_KEY_ID='key' \
  -e S3_SECRET_ACCESS_KEY='secret' \
  -e S3_BUCKET='bucket' \
  -e S3_PREFIX='prefix' \
  -e S3_REGION='region' \
  d3ividdy/mysql-bk-s3:latest
```

## Build & publish

```sh
docker build -f Dockerfile -t d3ividdy/mysql-bk-s3:latest . --no-cache
docker push d3ividdy/mysql-bk-s3:latest
```
