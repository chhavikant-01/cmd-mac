# cmd-mac
common commands I use

## Lists all processes listening on network ports
```sh
sudo lsof -i -P | grep LISTEN
````
-   `-i` shows network connections.
-   `-P` prevents port number resolution to service names.
-   `grep LISTEN` filters listening ports.

## Find the Process ID (PID) of the Port
```sh
sudo lsof -i :<PORT>
```

## Kill the Process
```sh
kill <PID>
```

## Reverse proxy
```sh
brew install ngrok
```
```sh
ngrok config add-authtoken <NGROX_TOKEN>
```
```sh
ngrok http --url=<YOUR_FORWARDING_URL> <LOCAL_PORT>
```
