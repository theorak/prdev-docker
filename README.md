



DB Backup and Restore
$ docker exec prdev-db sh -c 'exec mysqldump --all-databases -uroot -p"$MARIADB_ROOT_PASSWORD"' > /some/path/on/your/host/all-databases.sql

$ docker exec -i prdev-db sh -c 'exec mysql -uroot -p"$MARIADB_ROOT_PASSWORD"' < /some/path/on/your/host/all-databases.sql