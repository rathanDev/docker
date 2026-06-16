docker ps -a 

# Remove mssql container
docker rm mssql 

docker rm -f mssql 

# Remove mssql volume if exists
docker volume ls 

docker volume rm <volume_name>


# Create a new SQL Server container with a new SA password

docker run -d \
  --name mssql \
  -e "ACCEPT_EULA=Y" \
  -e "MSSQL_SA_PASSWORD=MyStrongPass@123" \
  -p 1433:1433 \
  mcr.microsoft.com/mssql/server:2022-latest


# Check if it started 
docker ps 

# Check logs
docker logs mssql


