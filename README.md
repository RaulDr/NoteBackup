# NoteBackup

This is a basic android note saver app. It can save notes on your phone, and even more, it will save them on
a remote server. It offers a backup for your notes. The server side is write in spring framework and the db 
runs on a docker container and is created by jpa. The android side db is created by sqlite.

## Tools 

- Android Studio
- spring framework
- Docker
- git

## Commands for server db docker container:

docker run --name notebackupdb -p 32770:5432 -d postgres

docker container update --restart=always notebackupdb

docker exec -it notebackupdb psql --username postgres -c "CREATE DATABASE notebackup OWNER postgres;"

docker exec -it notebackupdb psql --username postgres -c "GRANT ALL PRIVILEGES ON DATABASE notebackup TO postgres;"

## Some screenshot:
### Database
![DATABASE](https://github.com/RaulDr/NoteBackup/blob/master/res_images/2018-12-31_15h13_13.png)

###Frontend android app
![Main no notes](https://github.com/RaulDr/NoteBackup/blob/master/res_images/Screenshot_20181231-151026_NotesBackup.jpg)

![Add Note](https://github.com/RaulDr/NoteBackup/blob/master/res_images/Screenshot_20181231-151040_NotesBackup.jpg)

![Main with Notes](https://github.com/RaulDr/NoteBackup/blob/master/res_images/Screenshot_20181231-151237_NotesBackup.jpg)
