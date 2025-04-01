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
## Prisma Schema Update
```sh
npx prisma generate
```
```sh
npx prisma migrate dev --name did_this_update  # for development
```
## Start PostgreSQL
```sh
brew services start postgresql
```
### Get All Users
```sh
psql -c "\du" postgres
```

### Get Port of your database ( db name is your username by default )
```sh
psql -c "SHOW port;"
```

### Create DB
```sh
createdb dbname
```

### Connect to DB
```sh
psql -d dbname
```
### Utility
1. `\l` - List all databases
2. `\c database_name` - Connect to a specific database
3. `\dt` - List all tables in the current database
4. `\dt+` - List all tables with additional details
5. `\d table_name` - Describe a specific table's structure
6. `\du` - List all users/roles
7. `\df` - List all functions
8. `\dv` - List all views
9. `\dn` - List all schemas
17. `\?` - Show help for all psql commands
18. `\h [command]` - Get syntax help on a specific SQL command
19. `\q` - Quit/exit psql
20. `\password [username]` - Change a user's password securely
21. `\conninfo` - Display current connection information
23. `\s` - Display command history

You can see all available commands by typing `\?` at the psql prompt.
## Connect to EC2
```sh
# ensure your .pem file has proper permissions
chmod 400 your-key-file.pem
```
```sh
# for Ubuntu AMIs
ssh -i your-key-file.pem ubuntu@your-instance-public-dns
```
