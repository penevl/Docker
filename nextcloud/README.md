# Nextcloud and MariaDB stack
This stack consists of the linuxserver docker image of Nextcloud and the official MariaDB image.
> Note: If you are setting this up you only for a small group of people you can remove MariaDB from the stack as well as the USER,PASSWD and ROOT_PASSWD env variables.

Explanation of all the env variables
1. BASE_PATH - Where all the MariaDB and Nextcloud data is stored. On first launch in the specified directory there will be two additional folders created. One is `nextcloud` where all nextcloud files are stored and the other one is `db` where all the MariaDB files are stored. Make sure you have backups of this.
2. PORT - The port on which nextcloud will be made accessible.
3. TIMEZONE - A unix timezone
4. USER - The username for the database user and NOT the nextcloud admin user.
5. PASSWD - The password for USER
6. ROOT_PASSWD - The password for the database root user.

# Setting up nextcloud without MariaDB
This is not recommended for a deployment where there will be more then a few people using the service.  To set this up just set the data dir to `/data/` on first launch setup.

# Setting up nextcloud to use MariaDB

To make nextcloud use the mariadb databse after first launch choose an admin account user name and password. Then click on the `Storage & database` dropdown button and select `MySQL/MariaDB`. For `Database user` put the value of whatever you set the `USER` variable in the `.env` file and for the `Database password` put the value of what you set  the `PASSWD` variable. For `Database name` put `nextcloud`(case sensitive) and for `Database host` put `database:3306`.