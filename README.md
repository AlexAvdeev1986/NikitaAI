# NikitaAI
 NikitaAI site


Шаг 2: Локальный запуск на Fedora 42Установка Docker (если не установлен)

# Установка Docker
sudo dnf install docker docker-compose -y

# Запуск и автозагрузка Docker
sudo systemctl start docker
sudo systemctl enable docker

# Добавление пользователя в группу docker
sudo usermod -aG docker $USER
newgrp docker


3. Запустите контейнер:

# Запустите контейнер
docker-compose up -d

# Проверьте статус
docker-compose ps

# Просмотрите логи
docker-compose logs -f

Теперь сайт доступен по адресу: http://localhost
Шаг 3: Развертывание на Ubuntu 22 с HTTPS
3.1 Установка необходимых компонентов на сервере

# Обновление системы
sudo apt update && sudo apt upgrade -y

# Установка Docker
sudo apt install docker.io docker-compose -y

# Установка Nginx (для проксирования)
sudo apt install nginx certbot python3-certbot-nginx -y


3.2 Загрузите проект на сервер

# Создайте директорию
mkdir -p /opt/nikitaai
cd /opt/nikitaai

# Загрузите файлы (используйте scp, git или другой метод)


3.3 Обновите конфигурацию Nginx для контейнера
Файл nginx/your-site.conf:

server {
    listen 80;
    server_name nikitaai5151.serveminecraft.net;
    root /usr/share/nginx/html;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}

3.4 Обновите docker-compose.yml



# Запуск Docker
sudo systemctl start docker
sudo systemctl enable docker


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

