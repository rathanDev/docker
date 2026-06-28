mkdir airflow 
cd airflow 

curl -LfO https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml

mkdir -p ./dags ./logs ./plugins ./config

echo -e "AIRFLOW_UID=$(id -u)" > .env

docker compose up airflow-init

docker compose up
or
docker compose up -d

# UI
http://localhost:8080

# Default Credentials 
Username: airflow
Password: airflow


docker ps 
docker compose down
docker compose restart
docker compose logs -f 
docker exec -it airflow-scheduler airflow jobs check
