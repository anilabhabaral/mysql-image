# mysql image for testing

Run the below command to Install Docker

```
sudo apt update
sudo apt install docker.io
```
 
Grant a specific(Example ubuntu) user permission to docker deamon.

```
sudo su - 
usermod -aG docker ubuntu
systemctl restart docker
```

Clone Repo:
```
git clone https://github.com/anilabhabaral/mysql-image.git
cd mysql-image
```

Build image locally:
```
docker build . --file my-mysql/Dockerfile --tag mysql_img:latest
```
Run the image locally:
```
docker run -d -p 3306:3306 --name my-mysql -e MYSQL_ROOT_PASSWORD=supersecret mysql_img:latest
```
