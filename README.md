# marhaba-docker-react-api-vite
**api**
docker build -t docker-api .
docker run --name docker-api -d --network api-network -p 3000:3000 docker-api
**database**
docker run -d --name mongo -v my-volume:/data/db --network api-network -e MONGO_INITDB_ROOT_USERNAME=mongoadmin -e MONGO_INITDB_ROOT_PASSWORD=password -e MONGO_INITDB_DATABASE=marhaba mongo
**frontend**
docker build -t docker-front .
docker run --name docker-front -d -p 5173:5173 docker-front
