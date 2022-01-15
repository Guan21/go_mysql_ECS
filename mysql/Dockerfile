#使うDockerイメージ
FROM mysql:8.0
#ポートを開ける
EXPOSE 3306
#MySQL設定ファイルをイメージ内にコピー
ADD ./my.cnf /etc/mysql/conf.d/my.cnf
COPY ./init/1_create.sql /docker-entrypoint-initdb.d/
#docker runに実行される
CMD ["mysqld"]