# Monitoring instructions
1. Pick out a suitable location where all the data for the containers can be stored and make that the value for `BASE_PATH` in the .env file.
2. In that base location create 2 folders one named `loki` and the other `promtail`.
3. In the promtail dir paste the [promtail-config.yml](https://github.com/penevl/Docker/blob/main/monitoring/promtail/promtail-config.yml) file and in the `loki` dir place the [loki-config.yml](https://github.com/penevl/Docker/blob/main/monitoring/loki/loki-config.yml) file.
4. Install the loki driver for Docker with the command.
```
docker plugin install grafana/loki-docker-driver:latest --alias loki --grant-all-permissions
```
5. Edit the `daemon.json` file in the `/etc/docker/` direcotry and append the following lines to it.
```json
{
    "log-driver": "loki",
    "log-opts": {
        "loki-url": "http://localhost:3100/loki/api/v1/push",
        "loki-batch-size": "400"
    }
}
```
<b>NOTE: The file might not exist so you will need to create it.</b>

6. If you edit `LOKI_PORT` in the .env file make sure that it matches what the port is set to in the `promtail-config.yml` file under the option `clients` and then `url`
