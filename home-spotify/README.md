# Navidrome and web version of yt-dlp
This stack consists on navidrome and a version of yt-dlp with a webui ~~for easy pirating of music~~

Explenation of all env variables.
1. BASE_PATH - The directory where all the music files will be stored and navidrome config files will be stored. Make sure to have backups of this.
2. NAVIDROME_PORT - The port on which navidrome will be made accessible.
3. YTDLP_PORT - The port on which the yt-dlp webui will be made accessible on. Keep in mind that this webui does not have any sort of user authentication/login method so you will have to set somethig up like nginx access rules.