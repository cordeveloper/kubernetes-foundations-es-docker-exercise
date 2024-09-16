# Usa la imagen oficial de MongoDB versión 7.0.5 como base
FROM mongo:7.0.5

WORKDIR /app/data

COPY ratings_data.json .

RUN mkdir -p /docker-entrypoint-initdb.d

COPY script.sh /docker-entrypoint-initdb.d/

RUN chmod +x /docker-entrypoint-initdb.d/script.sh

EXPOSE 27017

