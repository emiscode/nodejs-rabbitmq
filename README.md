## NodeJs Consumer and Publisher with RabbitMQ
Simple consumer and publisher example
### Spin rabbitmq server docker
docker run --name rabbitmq -p 5672:5672  -d rabbitmq

### Spin rabbitmq server HTTP server docker

docker run --name rabbitmq -p 5672:5672 -p 15672:15672 -d rabbitmq:3-management

### HTTP (guest/guest)

{ headers: {"Authorization" : `Basic ${btoa('guest:guest')}`} }

http://localhost:15672/api/vhosts

http://localhost:15672/api/channels

http://localhost:15672/api/queues

### NODE
node publisher.js hello

node consumer.js