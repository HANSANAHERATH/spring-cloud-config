Run as Docker image 


Checkout https://github.com/HANSANAHERATH/config-properties.git 

mvn clean install -DskipTests=true


docker build -t config/cofig-service:latest .


docker run --name=cloud-config -p 8700:8888 -v E:/Works/config-properties:/config -e SPRING_CLOUD_CONFIG_SERVER_GIT_URI=file:/config -e spring.cloud.config.server.git.searchPaths=* -e spring.cloud.config.server.git.force-pull=false  config/cofig-service:latest


http://localhost:8700/app1/app1