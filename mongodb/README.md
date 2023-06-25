# MongoDB and MongoExpress Stack
If you do not want to have mongo-express you can remove the service in the docker-compose file and also all the `WEB_*` environment variables. 

Explenation of all the env variables

1. DATA_DIR - Where all the mongodb files are stored. Make sur eto have backups of this in a prod environment.
2. DB_PORT - The port on which mongodb will be accessible on.
3. WEB_PORT - The port on which mongo-express will be accessible on.
4. WEB_USER - The user which you can log in to mongo-express with
5. WEB_PASSWORD - The password for the WEB_USER
6. DB_USER - The user which you can log in to the database with
7. DB_PASSWD - The password for the DB_USER