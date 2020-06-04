FROM ubuntu

ENV CONTAINER_APP_PATH=/laravel

RUN apt-get update && \
    apt-get install -y git

CMD git clone https://github.com/laravel/laravel.git $CONTAINER_APP_PATH

docker run --detach --name db-server --publish 3306:3306 --env MYSQL_ROOT_PASSWORD=root-password --env MYSQL_DATABASE=laravel --env MYSQL_USER=laravel-user --env MYSQL_PASSWORD=laravel-user-password --volume /home/katred/laravel-docker/db-src/:/var/lib/mysql mysql