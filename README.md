# NikitaAI
 NikitaAI site


Запустите контейнеры. Из папки с docker-compose.yml выполните команду:

docker compose up -d

sudo docker run -d -p 8080:80 --name NikitaAI -v $(pwd):/usr/share/nginx/html nginx

# Просмотр логов контейнера
sudo docker logs NikitaAI

# Просмотр логов в реальном времени
sudo docker logs -f NikitaAI

# Остановить контейнер
sudo docker stop NikitaAI

# Запустить остановленный контейнер
sudo docker start NikitaAI

# Перезапустить контейнер
sudo docker restart NikitaAI

# Удалить контейнер
sudo docker rm NikitaAI

