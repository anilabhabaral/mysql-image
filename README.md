# mysql-docker test image

Build image locally:
```
docker build . --file my-mysql/Dockerfile --tag mysql_img:latest
```
Run the image locally:
```
docker run -d -p 3306:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=supersecret mysql_img:latest
```
