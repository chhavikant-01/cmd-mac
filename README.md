# cmd-mac
common commands I use
```sh
sudo lsof -i -P | grep LISTEN
````
-   Lists all processes listening on network ports.
-   `-i` shows network connections.
-   `-P` prevents port number resolution to service names.
-   `grep LISTEN` filters listening ports.
