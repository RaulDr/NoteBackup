# NoteBackup

docker run --name notebackupdb -p 32770:5432 -d postgres

docker container update --restart=always notebackupdb

docker exec -it notebackupdb psql --username postgres -c "CREATE DATABASE notebackup OWNER postgres;"

docker exec -it notebackupdb psql --username postgres -c "GRANT ALL PRIVILEGES ON DATABASE notebackup TO postgres;"