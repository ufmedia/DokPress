# Dockpress

A complete [Docker Compose](https://docs.docker.com/compose/) local development environment for Wordpress.

Once you're got [Docker](https://www.docker.com/get-started) installed on your local machine, clone this repo, remove the remote "git remote remove origin" and use the command:

```
docker compose up
```

## Database

You can provide an initial database .sql file in local/init-db which will get imported on first launch.

To ensure persistence of your database all files are stored locally in local/mysql-data.

### PhpMyAdmin

PhpMyAdmin is available at http://localhost:8080

## Wordpress

For persistence all files are stored locally in the root of the project. 

## Themes

Come back for more later.

## Plugins

Come back for more later.


