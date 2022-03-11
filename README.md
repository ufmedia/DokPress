# docker-wp-local

A complete [Docker Compose](https://docs.docker.com/compose/) local development environment for Wordpress.

Once you're got [Docker](https://www.docker.com/get-started) installed on your local machine, clone this repo, remove the remote "git remote remove origin" and use the command "docker-compose up".

A small number of otions can be found in the .env file.

Development and production credentials are differenciated by the getenv_docker('DEVELOPTMENT', 'PRODUCTION') function within the wp-config.php file.

## Database

You can access phpmyadmin at http://localhost:8081 and export/import your database.

You can also provide an initial database in src/init-db in .sql format which will get exported on first launch.

## Wordpress

All Wordpress files and folders will be added to the www folder which you can then use as the web root on your production server. This folder is mounted on your local file system for editing within your chosen IDE/Editor. 

## Themes

This repo includes two themes, horizon-bs and horizon-wind.

### horizon-bs

This is a fully working Wordpress theme which uses Bootstrap 5 and webpack. It's a little dated and bloated in places, but provides a very quick and clean starting point for rapid template development.

Within the theme folder run "npm install && npm run watch-sync" to start a browsersync session on http://localhost:3000

When you're ready to commit to production, run "npm run production"

### horizon-wind

Also fully working, but a work in progres. Based on tailpress this theme is intended to replace horizon-bs, at least on small sites where the bulk of bootstrap isn't required.

Within the theme folder run "npm install && npm run watch-sync" to start a browsersync session on http://localhost:3000

When you're ready to commit to production, run "npm run production"

### Custom themes

If you're setting up an existing website or running Wordpress headlessly, the horion themes can be removed in place of your own.

You can copy over the src, dist, package.json, tailwind.config.js and postcss.config.js files/folders from the horizon themes to utilise bootstrap or tailwind within your theme or just make use of the webpack scripts and browsersync.
