1. Clone this repo
2. Run `npm install`
3. Run `npm start`
4. You must add your own API key in the `controllers/image.js` file to connect to Clarifai API.

get Clarifai API key [here](https://www.clarifai.com/)

** Make sure you use postgreSQL instead of mySQL for this code base.
  
# Redis Sessions + JWT Auth

# AWS
* serverless aws template
* serverless aws IAM credentials
* Lambda invoke and deploy

# Docker

docker build -t NAME  
docker run -it NAME  
  
docker run -it -d NAME === run container in the background  
docker run -it -p 3000:3000 NAME === run container PORT 3000 CONTAINER FORWARDS TO PORT 3000 HOST MACHINE  
docker ps ============ list containers currently running  
docker container ls === list containers running?  
docker ps -a ==== list running and stopped containers  
  
docker exec -it ID(HASH) bash ==== access running container  
docker stop ID(HASH)  
  
// Dockerfile  
  
WORKDIR /usr/src/smart-brain-api === set working dir  
COPY ./ ./  
RUN npm install  
  
forward ports like this === it doesnt do it by default  
docker-compose run --service-ports  
docker-compose up  
  
docker-compose up --build ==== for all containers  
docker-compose up -d +++++ docker-compose exec smart-brain-api bash === get it up in the background then get inside  
docker-compose down  
  
  

!!!remove everything!!!  
powershell:   
  
docker rm $(docker ps -aq)  
docker network prune -f  
docker rmi -f $(docker images --filter dangling=true -qa)  
docker volume rm $(docker volume ls --filter dangling=true -q)  
docker rmi -f $(docker images -qa)  
  
docker ps  
docker exec -it idd bash  
psql -U clau -d smart-brain-docker  
\c smart-brain-docker  
\l === psql list dbs  
\dt === psql list tables  
SELECT * FROM users;
