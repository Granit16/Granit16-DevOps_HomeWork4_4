# Granit16-DevOps_HomeWork4_4

# Домашнее задание по занятию "Оркестрация группой Docker контейнеров на примере Docker Compose."

# Задача 1
https://hub.docker.com/repository/docker/granit16/custom-nginx/general

# Задача 2
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%202.png?raw=true)


# Задача 3

## п.п. 1 - 3
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.1-3.png?raw=true)

Контейнер работает пока выполняется какая-либо комадна на нем. После нажатия комбинации Ctrl-C остановилось выполнение комнады и контейнер остановился.

## п.п. 4 - 6
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.4-6.png?raw=true)

## п. 7
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.7.png?raw=true)

## п. 8
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.8.png?raw=true)

## п.п. 9-10
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.9-10.png?raw=true)

При запуске контейнера мы указали проброс 80 порта, а теперь сервер слушает порт 81 


## п. 11
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.11.png?raw=true)

## п. 12
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%203.12.png?raw=true)


# Задача 4

![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%204.png?raw=true)


# Задача 5

## п. 1
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.1.png?raw=true)

В соответствии с документацией, docker compose преимущественно выбирает файл с именем "compose.yaml" (или .yml), поддержка файлов с именем "docker-compose.yaml" (или .yml) осталась для обратной совместимости


## п. 2
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.2.png?raw=true)

## п. 3
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.3.png?raw=true)

## п.п. 4-6
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.4-6.png?raw=true)

## п. 7
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.7.png?raw=true)

Docker compose выдал предупреждение о наличии контейнера без описания инфраструктуры и предложил удалить его

## Скриншот portainer c задеплоенным компоузом
![alt text](https://github.com/Granit16/Granit16-DevOps_HomeWork4_4/blob/main/%D0%94%D0%974%20%D0%97%D0%B0%D0%B4%D0%B0%D1%87%D0%B0%205.%2B.png?raw=true)

## Содержимое compose.yaml
version: "3"
include:
  - docker-compose.yaml
services:
  portainer:
    image: portainer/portainer-ce:latest
    network_mode: host
    ports:
      - "9000:9000"
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock


