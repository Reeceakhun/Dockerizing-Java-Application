FROM mysql:8.0.33
LABEL "project"="Dockerizing-Java-Application"
LABEL "Author"="Reece"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MSQL_DATABASE="accounts"

COPY db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql/
RUN chmod +x /docker-entrypoint-initdb.d/db_backup.sql

