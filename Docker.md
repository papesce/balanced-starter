# create and run development version
docker-compose -f docker-compose.dev.yml -p balanced-starter-dev up

# creates and run production version
docker-compose -f docker-compose.prod.yml -p balanced-starter-prod up

# create image for production (portforward to http://localhost:80)
docker run -p 80:80 --name balanced-starter-app balanced-starter-prod