
docker-compose -v
docker-compose config
docker-compose up           (-d)
docker-compose ps 
docker-compose down

docker ps 
    ID 

docker exec it <ID> bash 

psql 

\l              show databases
\c  dbName      connect to database
\dn             list all schemas 
\dt             list all tables 



interview_accountapi=# \d "Account";


insert into "Account"(id, organisation_id, version, is_deleted, is_locked, created_on, modified_on, record) values ('f50fc252-03f3-11ed-a0bc-0242ac130003', 'f50fc252-03f3-11ed-a0bc-0242ac130004', 1, false, false, '2022-01-01', '2022-02-02', '{"key1": "value1", "key2": "value2"}');


delete * from "Account";

select * from "Account";

