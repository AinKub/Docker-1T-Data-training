# Docker-1T-Data-training

## Starting a single database
1. Move to db folder - `cd db`
2. Build image by using command `docker build -t test_image:latest .`
3. Run container - `docker run -d -p 5432:5432 --name test_container test_image:latest`
4. Check the container by using `docker ps`

Finally, the result will be as follows:
![Worked postgres](img/worked_postgres.png)

## Connecting to database in container
In order to connect to the created test database, you need to run the following command:
```
docker exec -it test_container psql -U test -d test_db
```
This will open the psql shell
![psql shell](img/psql_shell.png)

And we can execute several commands in the table
```
test_db=# \dt
test_db=# SELECT * FROM index_mass;
```
![Database checking](img/database_checking.png)