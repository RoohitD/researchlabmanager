
## Running the microsoft SQL server

docker run --platform linux/amd64 --cap-add SYS_PTRACE -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=YourStrongPassword123!' -p 1433:1433 --name sql_server_2025 -d mcr.microsoft.com/mssql/server:2025-latest

docker exec -u 0 -it sql_server_2025 chmod 644 /var/opt/mssql/backup.bak

docker cp /Users/rohitdeshmukh/Documents/NJIT/NJIT_Spring_2026/DBMS/DBMS/ResearchLabManager.bak sql_server_2025:/var/opt/mssql/backup.bak
