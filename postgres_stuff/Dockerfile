FROM postgres:9.6-alpine
ADD ./postgres_dbs_script/init_postgres_dbs.sh /docker-entrypoint-initdb.d/
ENTRYPOINT ["docker-entrypoint.sh"]
EXPOSE 5432
CMD ["postgres"]
