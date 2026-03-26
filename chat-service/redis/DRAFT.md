docker build -t my-redis . 

docker run -d \
    -- name redis
    -p 6379:6379 \
    my-redis

docker exec -it redis redis-cli

> KEYS *
