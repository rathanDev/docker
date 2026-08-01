version: "3.9"

services:
  oracle-db:
    image: container-registry.oracle.com/database/free:latest
    container_name: oracle-db
    ports:
      - "1521:1521"
      - "5500:5500"
    environment:
      ORACLE_PWD: oracle
    volumes:
      - oracle-data:/opt/oracle/oradata
    restart: unless-stopped

volumes:
  oracle-data: