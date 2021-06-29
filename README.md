# Wordpress Bedrock with Lando Starter
This is a starter repo for creating a project with Lando 3 and Bedrock

## Install Requirements
Docker (if you don't already have it)
* https://docs.docker.com/get-docker/

Lando
* https://docs.lando.dev/basics/installation.html

### Download this repo
```
git clone https://github.com/Cmac2712/wordpress-bedrock-lando-starter.git
```

### Remove .git 
```
git remote remove origin
```

### Copy .lando.yml.example to .lando.yml and edit the name and URL of your project
```
name: PROJECT_NAME
recipe: wordpress
proxy:
  appserver_nginx:
    - PROJECT_URL
```

### Copy .env.example to .env with the URL of your project
```
WP_HOME=https://PROJECT_NAME.lndo.site
WP_SITEURL=https://PROJECT_NAME.lndo.site/wp
```

#### IMPORTANT
If you want to use a URL other than ``*.lndo.site`` who will have to add ``127.0.0.1`` to your ``/etc/hosts`` file

### Start Lando
```
lando start
```

## Get DB and site info
```
lando info
```
