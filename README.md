
# Minio with Laravel and AWS S3
```
mkdir data
docker-compose up -d
```
# Access panel 

Access http://localhost:9001 with default access and secret key and create a bucket

# Connect to your php container
```
docker network connect minio_minio yourphpcontainer
```
# Use docker service name in the host config

* region is irrelevant
```
FILE_SYSTEM=s3
AWS_ACCESS_KEY_ID=minioadmin
AWS_SECRET_ACCESS_KEY=minioadmin
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=bucket
AWS_ENDPOINT=http://minio:9000
```
# Test with tinker

Enter:
```
php artisan tinker

Storage::cloud()->put('hello.json', '{"hello": "world"}');
```
# More information:

https://docs.min.io/docs/minio-quickstart-guide.html
