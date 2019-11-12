#lastupdate
this is packaged as zip and uploaded into system  2019-11-07 18:00
# git init

git add *

git commit -m "first commit"

git remote add origin https://github.com/woyaowoyao/fullstacksba.git

git push -u origin master



# fullstacksba
 cd service-registry & mvn clean package & docker build -t robin9999/service-registry:sba1 . 
 cd user-auth & mvn clean package & docker build -t robin9999/users:sba1 .
 cd payments & mvn clean package & docker build -t robin9999/payments:sba1 . 
 cd FrontEnd &  docker build -t robin9999/FrontEnd:sba1 . 
 cd zuulgateway  & mvn clean package& docker build -t robin9999/zuulgateway:sba1 . 
 cd trainings  & mvn clean package& docker build -t robin9999/trainings:sba1 .
 cd technology-skill  & mvn clean package& docker build -t robin9999/technology:sba1 .
 
 
 cd.. & cd docker-compose & docker-compose -f docker-compose.yml up -d
 
 open browser http://localhost:9000/
 #jenkins
 
 docker run -u root  --rm -d -p 7001:8080 -p 50000:50000 -v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock  robin9999/blueocean4docker:v1
 setup jenkins
 create job
 
X-XSRF-TOKEN: 834936ee-b812-4d32-b6f1-5b04d03eb1a9

X-XSRF-TOKEN: fd55464f-e69a-4207-abe6-1252dd1578ee