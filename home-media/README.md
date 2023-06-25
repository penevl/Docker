# Jellyfin and web version of qbittorrent
This stack consists of jellyfin and a version of qbittorent with a webui for easily sorting through your linux ISOs.

Explenation of all env variables. 
1. BASE_PATH - The place where all movies and config files will be stored. Make sure to have backups of this.
2. QBT_WEB_PORT - The port on which qbittorent will be made accessible on.
3. JELLYFIN_PORT - The port on which jellyfin will be made accessible on.
4. TIMEZONE - A unix timezone. 

# Fixing qbittorent unauthorized error
When connecting to qbittorent you might get an error which just says `unauthorized`. The way to fix this is to edit the `BASE_PATH/config/qbittorent/qBittorrent/qBittorrent.conf` file and add these two lines at the bottom.
```
WebUI\HostHeaderValidation=false
WebUI\CSRFProtection=false
```