docker build --tag=logstash --force-rm=true .
docker tag 48045788a2f3 kris979/kb-logstash-7.6.1
docker push kris979/kb-logstash-7.6.1
docker run -d --net=host --name logstash -v "d:\logs:/api-logs" logstash
