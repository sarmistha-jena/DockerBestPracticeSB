<html><body><h1 style="font-size:50px;color:blue;">WEZVA TECHNOLOGIES (ADAM) <br> <font style="color:red;"> www.wezva.com <br> <font style="color:green;"> +91-9739110917 </h1>
<h1> PLEASE LIKE & SUBSCRIBE TO OUR YOUTUBE CHANNEL - DevOpsLearnEasy
    https://www.youtube.com/c/DevOpsLearnEasy </h1> </body></html>
              
# mavenbuild
## How to run it
```
# Build Jar & Skip Unit Test
$ mvn clean package -Dmaven.test.skip=true

# Run MySQL backend container for testing
$ docker run --name mydb -p 3306:3306 -e MYSQL_USER=wezvatech -e MYSQL_PASSWORD=password -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=mywezvadb -d mysql:8.1

# Check if mysql is working fine
$ docker exec -it mydb mysql -uroot -ppassword
  mysql> show databases;
  mysql> use mywezvadb;
  mysql> show tables;
  mysql> select * from books;

# Deploy the application
$ nohup java -jar target/wezvatech-springboot-mysql-9739110917.jar 2>&1 &

# Check if its up & running
$ curl -s http://localhost:8080/books

# Add a entry to test the application
$ curl -X POST -H "Content-Type: application/json" -d '{"title":"Book A", "price":49.99, "publishDate":"2024-04-12"}' "http://localhost:8080/books"


```

