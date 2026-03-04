# Отчет по практической работе №1
## Студент: СДС
## Группа: БСБО
## Дата выполнения: 05.03.2026
### 1. Выполненные команды Docker
#### 1.1 Работа с образами
![docker search nginx](screenshots/images/1.png)
![docker pull nginx:alpine](screenshots/images/2.png)
![docker images](screenshots/images/3.png)
![docker history nginx:alpine](screenshots/images/4.png)
![docker rmi nginx:alpine](screenshots/images/5.png)
![docker pull postgres:15-alpine](screenshots/images/6.png)
![docker pull golang:1.21-alpine](screenshots/images/7.png)
#### 1.2 Работа с контейнерами
![docker run -it --name test-alpine alpine:latest sh](screenshots/images/8.png)
![docker run -d --name web-server -p 8080:80 nginx:alpine docker ps](screenshots/images/9.png)
![docker ps -a](screenshots/images/10.png)
![docker logs web-server](screenshots/images/11.png)
![docker exec -it web-server sh cat /usr/share/nginx/html/index.html, exit](screenshots/images/12.png)
![docker stop web-server docker start web-server docker rm web-server](screenshots/images/13.png)
![docker exec -it my-postgres psql -U postgres -c 'SELECT version();'](screenshots/images/14.png)
#### 1.3 Работа с томами
![docker volume create SDS-app-data docker volume ls](screenshots/images/15.png)
![docker volume inspect my-app-data](screenshots/images/16.png)
![docker run -d](screenshots/images/17.png)
![docker exec -it postgres-db psql](screenshots/images/18.png)
![docker stop postgres-db](screenshots/images/19.png)
![docker rm postgres-db](screenshots/images/20.png)
![docker volume create static-html docker cp image](screenshots/images/21.png)
#### 1.4 Работа с сетями
![docker network create my-app-network](screenshots/images/22.png)
![docker exec app ping postgres](screenshots/images/23.png)
![docker network create my-bridge-net](screenshots/images/24.png)
![docker exec -it nginx-web ping -c 4 postgres-db](screenshots/images/25.png)
#### 1.4 Разработка приложения
![3.1 Backend на Go 3.2 Frontend и статика 3.3 Скрипты инициализации БД](screenshots/images/26.png)
![4.1 Dockerfile для Go приложения](screenshots/images/27.png)
![5.1 Создание Personal Access Token](screenshots/images/28.png)
![5.2 Настройка Secrets в репозитории](screenshots/images/29.png)
![5.4 Тестовый docker-compose для CI](screenshots/images/30.png)
### 2. Скриншоты работающего приложения
#### 2.1 Главная страница
![Главная страница](screenshots/main-page.png)
#### 2.2 Добавление пользователя
![Добавление пользователя](screenshots/add-user.png)
#### 2.3 Список пользователей в БД
![PostgreSQL](screenshots/postgres-data.png)
### 3. GitHub Actions
#### 3.1 Успешный запуск workflow
![GitHub Actions](screenshots/github-actions.png)
#### 3.2 Опубликованные образы в GHCR
![GHCR Packages](screenshots/ghcr-packages.png)
### 4. Выводы
В ходе выполнения практической работы я освоил базовые принципы работы с Docker и контейнеризацией приложений. Было изучено создание Docker-образов, запуск и управление контейнерами, работа с томами и сетями.

Также была настроена автоматическая сборка и публикация образов с использованием GitHub Actions.