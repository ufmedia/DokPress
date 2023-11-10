![GitHub contributors](https://img.shields.io/github/contributors-anon/ufmedia/dockpress) ![GitHub last commit (by committer)](https://img.shields.io/github/last-commit/ufmedia/dockpress)

![WordPress](https://img.shields.io/badge/WordPress-%23117AC9.svg?style=for-the-badge&logo=WordPress&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white) ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=for-the-badge&logo=php&logoColor=white)

# DockPress

A complete [Docker Compose](https://docs.docker.com/compose/) local development environment for WordPress.

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
    </li>
    <li>
      <a href="#plugins">Database</a>
      <ul>
        <li><a href="#import-an-existing-database">Import and Existing Database</a></li>
        <li><a href="#phpmyadmin">PhpMyAdmin</a></li>
      </ul>
    </li>
    <li><a href="#wordpress">Wordpress</a></li>
    <ul>
        <li><a href="#wp-cli">WP CLI</a></li>
        <li><a href="#themes">Themes</a></li>
      </ul>
    <li><a href="#testing">Testing</a></li>
    <li><a href="#further-reading">Further Reading</a></li>
  </ol>
</details>

## Getting Started

Once you've got [Docker](https://www.docker.com/get-started) installed on your local machine, clone this repo, remove the remote and start the containers:

```
git remote remove origin
docker compose up
```

## Database

To ensure persistence of your database all files are stored locally in local/var/lib/mysql.

Database credentials are set in the .env file:

```
DB_USER=wordpress
MYSQL_DATABASE=wordpress
MYSQL_ROOT_PASSWORD=wordpress
```
(Use these values when accessing the database via phpmyadmin too)

### Import an existing database

You can provide an initial database .sql file in local/initial-db which will get imported on first run of the database container.

### PhpMyAdmin

PhpMyAdmin is available at http://localhost:8080

## WordPress

By default we're using the version 6.4.0 of WordPress running on Apache PHP8.2 from the [official docker repo](https://hub.docker.com/_/wordpress), you can change this in the .env file:

```
WP_VERSION=6.4.0-php8.2-apache
```
For persistence all files are stored locally in the root of the project.

### WP CLI

WP CLI is installed on the Wordpress container, you can use your preferred method for connecting to and running commands on the container to make use of this e.g:

```
wp cli version
```

### Themes

Take a look at my fork of the official Timber (Twig based) quick start theme which itself is a fork of the _s theme: [Timberpress](https://github.com/ufmedia/timberpress). This theme includes basic TailwindCSS classes, enough to rapidly build your UI.

To compliment this theme check out my webpack solution for compiling SASS and JS, this includes Tailwind and PostCSS: [Tailpack](https://github.com/ufmedia/tailpack)

## Testing

I'm working on adding testing out of the box.

## Further reading

A work in progress.


