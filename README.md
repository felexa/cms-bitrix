,,,
version: '3'
services:
  web-master:
    container_name: a24
    image: "felexa/cms-bitrix:latest"
    ports:
      - "80:80"
      - "443:443"
    restart: always
    cap_add:
      - SYS_ADMIN
    security_opt:
      - seccomp:unconfined
    privileged: true
   volumes:
     - .:/home/bitrix/www



Для подключения проекта поменяйте значение `volumes` секции `web` на `path-to-project/:/home/bitrix/www`. 
