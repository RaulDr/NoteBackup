# NoteBackup

This is a basic android note saver app. It can save notes on your phone, and even more, it will save them on
a remote server. It offers a backup for your notes. The server side is write in spring framework.

## Tools 

- Android Studio
- spring framework
- Docker
- git

## Commands for server db docker container:

docker run --name notebackupdb -p 5432:32770 -d postgres

docker container update --restart=always notebackupdb

docker exec -it notebackupdb psql --username postgres -c "CREATE DATABASE notebackup OWNER postgres;"

docker exec -it notebackupdb psql --username postgres -c "GRANT ALL PRIVILEGES ON DATABASE notebackup TO postgres;"