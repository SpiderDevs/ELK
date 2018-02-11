https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation.html 

https://hub.docker.com/r/prima/filebeat/

Run
docker run -v filebeat.yml:/filebeat.yml --mount source=logs-volume,target=/app/Logs --restart always -d --name filebeat docker.elastic.co/beats/filebeat:6.2.1

FROM prima/filebeat
COPY my-config/filebeat.yml /filebeat.yml