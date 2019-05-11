# docker-tmserver
Docker image for simple or customizable Trackmania Nations Forever server

## How to use this image
```docker run -e {required environment variables} -p {selected ports} fanyx/tmserver```

### There are several required environment variables that you need to set:
  - `$SERVER_LOGIN`               | Server account login
  - `$SERVER_LOGIN_PASSWORD`      | Server account password
  - `$DB_HOST`                    | Hostname of the MySQL-Server
  - `$DB_NAME`                    | Name of the MySQL-Database
  - `$DB_LOGIN`                   | Name of the database user
  - `$DB_LOGIN_PASSWORD`          | Password to the database user
  
### Optional environment variables are:
  - `$SERVER_PORT`                | Port for server communications -> Default : 2350
  - `$SERVER_P2P_PORT`            | Port for peer2peer communication -> Default : 3450
  - `$SERVER_SA_PASSWORD`         | Password for SuperAdmin credential -> when left empty will be randomly generated
  - `$SERVER_ADM_PASSWORD`        | Password for Admin credential -> when left empty will be randomly generated
  - `$SERVER_NAME`                | Server name in ingame browser -> Default : "Trackmania Server"
  - `$SERVER_COMMENT`             | Server description -> Default : "This is a Trackmania Server"
  - `$SERVER_PASSWORD`            | If you want to secure your server against unwanted logins, set a server password

## Running this image with `docker-compose`
I have a default [`docker-compose.yml`](https://github.com/ryluth/docker-tmserver/blob/master/docker-compose.yml) included in this repository.
You can adjust this file to your needs but running with docker-compose is more comfortable in general.

## Further information
You can open volumes to the Trackmania server files and Xaseco files (`docker-compose` does this per default) and edit configuration files.
This is needed since the default track playlist just runs the white Nadeo tracks so i advise examining the config volumes to adjust the track playlist.
Furthermore you can edit the Xaseco plugins to your need and adjust ingame administrator accounts and so on.
