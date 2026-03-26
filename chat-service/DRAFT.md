# ----- ----- ----- -----

docker build -t my-redis . 

docker run -d \
    -- name redis
    -p 6379:6379 \
    my-redis

docker exec -it redis redis-cli

> KEYS *




# ----- ----- ----- -----





docker build -t my-mysql .

docker run -d \
    --name mysql \
    -p 3306:3306 \
    my-mysql





docker exec -it mysql mysql -u root -p

> root

ALTER USER 'admin'@'%' IDENTIFIED WITH mysql_native_password BY 'admin';
FLUSH PRIVILEGES;



1. Allow public key retrieval (quick fix)

In DBeaver, when creating the connection:

Edit connection → Driver Properties
Add property:
allowPublicKeyRetrieval = true
useSSL = false


# ----- ----- ----- -----


docker ps 

