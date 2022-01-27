# Getting Started
Nuevo Test
## Windows
​
### Clean, Compile, Test, Jar
* gradlew.bat clean build
​
### Run Jar
* Local:      gradlew.bat bootRun
* Background: nohup bash gradlew.bat bootRun &
​
### Testing Application
* Abrir navegador: http://localhost:8081/rest/mscovid/test?msg=testing
* curl -X GET 'http://localhost:8081/rest/mscovid/test?msg=testing'
## Linux
​
### Clean, Compile, Test, Jar
* gradle clean build
​
### Run Jar
* Local:      gradle bootRun
* Background: nohup bash gradle bootRun &
​
### Testing Application
* Abrir navegador: http://localhost:8081/rest/mscovid/test?msg=testing
* curl -X GET 'http://localhost:8081/rest/mscovid/test?msg=testing'
​
# Using Docker to test this app.
⚠️ **Is mandatory to use Powershell in Windows**
## Docker in Windows
```bash
### Clean, Compile, Test, Jar
docker run -it --rm -v ${pwd}:/code --workdir /code gradlew.bat clean build
​
### Run Jar
docker run -it --rm -p 9081:8081  -v ${pwd}:/code --workdir /code gradlew.bat bootRun
```
## Docker in Linux
```bash
### Clean, Compile, Test, Jar
docker run -it --rm -v $(pwd):/code --workdir /code gradle clean build
​
### Run Jar
docker run -it --rm -p 8081:8081  -v $(pwd):/code --workdir /code gradle bootRun
```