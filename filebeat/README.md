https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation.html 

https://hub.docker.com/r/prima/filebeat/

Run

docker build . --tag filebeat

docker run --mount source=logs-volume,target=/app/Logs --restart always -d --name filebeat filebeat

FROM prima/filebeat
COPY my-config/filebeat.yml /filebeat.yml