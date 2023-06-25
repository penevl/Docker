# Filebrowser
Filebrowser is a utility which allows you to access your fs through a secure webui. There are only 2 things which can be configured and one mandatory thing which you have to configure. The part which is mandatory is to create a `filebrowser.db` file in the directory which you are going to expose.

1. The webui port - To do this just edit the `8080` port in the docker-compose file.
2. The exposed directory - This is the directory which filebrowser will have access to. To change this edit the `exposed-dir` in the docker-compose file
