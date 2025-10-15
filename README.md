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

