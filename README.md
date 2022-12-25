# Docker

A repository to keep all my docker-compose files and/or docker stacks.

## Available stacks
1. [home-media](http://git.penevl.org/elduko/Docker/src/branch/main/home-media) - A stack consisting of [jellyfin](https://hub.docker.com/r/linuxserver/jellyfin) and [qbittorent](https://hub.docker.com/r/linuxserver/qbittorrent). Made to be deployed with docker-compose using a .env file
2. [home-spotify](http://git.penevl.org/elduko/Docker/src/branch/main/home-spotify) - A stack consisting of [navidrome](https://hub.docker.com/r/deluan/navidrome) and [yt-dlp](https://hub.docker.com/r/marcobaobao/yt-dlp-webui). Made to be deployed with docker-compose using a .env file
3. [filebrowser](http://git.penevl.org/elduko/Docker/src/branch/main/filebrowser) - A stack consisting of [filebrowser](https://hub.docker.com/r/filebrowser/filebrowser). Made to be deployed with docker-compose using a .env file
4. [monitoring](http://git.penevl.org/elduko/Docker/src/branch/main/monitoring) - A stack consisting of [promtail](https://hub.docker.com/r/grafana/promtail), [loki](https://hub.docker.com/r/grafana/loki) and [grafana](https://hub.docker.com/r/grafana/grafana) . Made to be deployed with docker-compose using a .env file