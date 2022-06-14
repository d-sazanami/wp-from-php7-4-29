FROM mysql:5.7.16

COPY docker/db/my.cnf /etc/mysql/conf.d/

RUN apt-get update && \
    apt-get install -y locales && \
    rm -rf /var/lib/apt/lists/* && \
    echo "ja_JP.UTF-8 UTF-8" > /etc/locale.gen && \
    locale-gen ja_JP.UTF-8
ENV LC_ALL ja_JP.UTF-8

CMD ["mysqld"]

EXPOSE 3306