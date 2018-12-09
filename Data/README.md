- Install postgresql

- In postgresql prompt
create database "dbname"

- \q

- psql -h ip -U postgres dbname < hr_database.pgsql
 hr_database.pgsql must be with proper path. For local machine ip is 127.0.0.1

- psql -h ip -U postgres dbname

- CREATE ROLE username WITH LOGIN ENCRYPTED PASSWORD 'password';

- GRANT CONNECT ON DATABASE dbname TO username;

- GRANT SELECT ON ALL TABLES IN SCHEMA public TO username;

- \q

- psql -h ip -U postgres dbname
supply password for username

- Start executing SQL commands now
