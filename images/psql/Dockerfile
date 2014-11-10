FROM postgres:9.3
ADD fix-acl.sh /docker-entrypoint-initdb.d/
ADD setup-my-schema.sh /docker-entrypoint-initdb.d/
EXPOSE 5432
