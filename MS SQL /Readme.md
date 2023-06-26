## 2022-latest

    docker pull mcr.microsoft.com/mssql/server:2022-latest

## 2019-latest

    docker pull mcr.microsoft.com/mssql/server:2019-latest

## 2017-latest

    docker pull mcr.microsoft.com/mssql/server:2017-latest

# Run

    docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Admin123" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2022-latest
