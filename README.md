**SETUP**

1) add secrets for passwords
$ mkdir secrets
$ echo "your-password" > ./secrets/db_password.txt
$ echo "your-root-password" > ./secrets/db_root_password.txt


**Xdebug configuration**
/build/<php-version>/php-ext-xdebug

**DB Backup and Restore**
$ docker exec prdev-db sh -c 'exec mysqldump --all-databases -uroot -p"$MARIADB_ROOT_PASSWORD"' > /some/path/on/your/host/all-databases.sql

$ docker exec -i prdev-db sh -c 'exec mysql -uroot -p"$MARIADB_ROOT_PASSWORD"' < /some/path/on/your/host/all-databases.sql