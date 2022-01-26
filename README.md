# Getting Started
Cambio realizado

## Windows

### Compile Code
* ./mvnw.cmd clean compile -e

### Test Code
* ./mvnw.cmd clean test -e

### Jar Code
* ./mvnw.cmd clean package -e

### Run Jar
* Local:      ./mvnw.cmd spring-boot:run 
* Background: nohup bash mvnw.cmd spring-boot:run &

### Testing Application
* Abrir navegador: http://localhost:8081/rest/mscovid/test?msg=testing

## Linux

### Compile Code
* ./mvnw clean compile -e

### Test Code
* ./mvnw clean test -e

### Jar Code
* ./mvnw clean package -e

### Run Jar
* Local:      ./mvnw spring-boot:run 
* Background: nohup bash mvnw spring-boot:run &

### Testing Application
* curl -X GET 'http://localhost:8081/rest/mscovid/test?msg=testing'

# Using Docker to test this app.
⚠️ **Is mandatory to use Powershell in Windows**
## Docker in Windows
```bash
### Compile Code
docker run -it --rm -v ${pwd}:/code --workdir /code maven mvn clean compile -e

### Test Code
docker run -it --rm -v ${pwd}:/code --workdir /code maven mvn clean test -e

### Jar Code
docker run -it --rm -v ${pwd}:/code --workdir /code maven mvn clean package -e

### Run Jar
docker run -it --rm -p 8081:8081  -v ${pwd}:/code --workdir /code maven mvn spring-boot:run
```
## Docker in Linux
```bash
### Compile Code
docker run -it --rm -v $(pwd):/code --workdir /code maven mvn clean compile -e

### Test Code
docker run -it --rm -v $(pwd):/code --workdir /code maven mvn clean test -e

### Jar Code
docker run -it --rm -v $(pwd):/code --workdir /code maven mvn clean package -e

### Run Jar
docker run -it --rm -p 8081:8081  -v $(pwd):/code --workdir /code maven mvn spring-boot:run
```