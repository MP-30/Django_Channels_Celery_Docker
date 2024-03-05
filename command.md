pip freeze > requirements.txt
sudo chmod +x ./entrypoint.sh
docker-compose up -d --build
./manage.py startapp taskapp
docker exec -it django /bin/sh