#STEPS TO RUN THIS APPLICATION

docker rmi -f $(docker images -a -q)
docker pull mysql
docker images
docker network create curd-web-app-mysql-net
docker network ls
docker ps
docker run --name mysqldb --network curd-web-app-mysql-net -e MYSQL_ROOT_PASSWORD=Satyam@123456 -e MYSQL_DATABASE=aryanDb -d mysql
docker exec -it mysqldb bash
mysql -u root -p
./gradlew clean build
docker build -t curd-web-app .
docker run --network curd-web-app-mysql-net --name springboot-mysql-container -p 8080:8080 curd-web-app
http://localhost:8080/api/v1/employees