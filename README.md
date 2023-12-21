# PROJET-DOCKER

  Nous avons une VM. On récupère l'adresse ip de cette vm : 
ifconfig

  connexion ssh
ssh david@198.168.1.45

  On importe postgre et redis
 docker pull redis
 docker pull postgres:15-alpine

   On lance le registry
docker run -d -p 5000:5000 --restart always --name registry registry:2

  On tag redis et postgre
docker tag postgres:15-alpine localhost:5000/postgres:15-alpine
docker tag redis:latest localhost:5000/redis:latest

  On crée ensuite un git clone : 
git clone https://github.com/yoniMICHARD/ynov-resources.git

  On lance ensuite le chemin :
cd ynov-resources/2023/m2/dataeng$ cd humans-best-friend/

  On créer ensuite le docker-compose.build.yml:
 vi docker-compose.build.yml

   On crée ensuite le docker-compose :
 vi docker-compose.yml

 On lance ensuite le docker commpose build :
docker compose -f docker-compose.build.yml up -d

  Puis le docker compose :
docker compose up -d
