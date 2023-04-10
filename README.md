# Employee-Management-Three-Tier-App

- sudo apt update and sudo apt upgrade -y
- sudo apt-get install mysql-server –y
- sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
- Bind IP all
- sudo mysql -u root -p
- password - root
- create user 'tom'@'%' identified by 'root';
- create database kube;
- GRANT ALL PRIVILEGES ON kube.* TO 'tom'@'%';

App

- git clone https://github.com/14Rahul/Employee-Management-Three-Tier-App.git
- sudo apt-get install maven default-jre
- vi /employee-mgmt/springboot-backend/src/main/resources/application.properties and add dbip and port
	- spring.datasource.url=jdbc:mysql://localhost:3306/kube?createDatabaseIfNotExist=true&allowPublicKeyRetrieval=true&useSSL=false&user=tom$password=root
- vi /employee-mgmt/springboot-backend/src/main/java/net/javaguides/springboot/controller/EmployeeController.java
	- @CrossOrigin(origin={"*"})
- /employee-mgmt/springboot-backend/
- mvn clean install
- /employee-mgmt/springboot-backend/target/
- java -jar -Djava.net.preferIPv4Stack=true jarfile &


Web

- sudo apt-get install npm
- sudo npm update npm -g
- vi /employee-mgmt/react-frontend/src/services/EmployeeService.js
	- const EMPLOYEE_API_BASE_URL = "http://localhost:8080/employees";
- cd /employee-mgmt/react-frontend/
- npm i
- npm start$
