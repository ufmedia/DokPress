![GitHub contributors](https://img.shields.io/github/contributors-anon/ufmedia/dockpress) ![GitHub last commit (by committer)](https://img.shields.io/github/last-commit/ufmedia/dockpress)



# DockPress

A complete [Docker Compose](https://docs.docker.com/compose/) local development environment for WordPress.

Once you've got [Docker](https://www.docker.com/get-started) installed on your local machine, clone this repo, remove the remote "git remote remove origin" and use the command:

```
docker compose up
```

## Database

To ensure persistence of your database all files are stored locally in local/var/lib/mysql.

#### Import an existing database

You can provide an initial database .sql file in local/initial-db which will get imported on first run of the database container.

#### PhpMyAdmin

PhpMyAdmin is available at http://localhost:8080

## WordPress

By default we're using the version 6.3.1 of WordPress running on Apache PHP8 from the [official docker repo](https://hub.docker.com/_/wordpress), you can change this in the .env file:

```
WP_VERSION=6.3.1-php8.0-apache
```

Database credentials are also set in the .env file and are used by both the WordPress and MySQL containers:

```
DB_USER=wordpress
MYSQL_DATABASE=wordpress
MYSQL_ROOT_PASSWORD=wordpress
```
(Use these values when accessing the database via phpmyadmin too)

For persistence all files are stored locally in the root of the project. Depending on your server setup you'll want to remove the core wordpress files and folders from the .gitignore file.

## Themes

Take a look at my fork of the official Timber (Twig based) quick start theme which itself is a fork of the _s theme: [Timberpress](https://github.com/ufmedia/timberpress). This theme includes basic TailwindCSS classes, enough to rapidly build your UI.

To compliment this theme check out my webpack solution for compiling SASS and JS, this includes Tailwind and PostCSS: [Tailpack](https://github.com/ufmedia/tailpack)




