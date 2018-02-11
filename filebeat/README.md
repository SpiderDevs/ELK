https://www.elastic.co/guide/en/beats/filebeat/current/filebeat-installation.html 

https://hub.docker.com/r/prima/filebeat/

Run
docker run -v /path/to/filebeat.yml:/filebeat.yml docker.elastic.co/beats/filebeat:6.2.1
Or, you can create your own derived image, with the configuration in the image itself.

FROM prima/filebeat
COPY my-config/filebeat.yml /filebeat.yml