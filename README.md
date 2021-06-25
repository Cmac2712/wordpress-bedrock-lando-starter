# Wordpress Bedrock with Lando Starter

## Install Requirements
Docker (if you don't already have it)
* https://docs.docker.com/get-docker/

Lando
* https://docs.lando.dev/basics/installation.html

### Download this repo
```
git clone git@bitbucket.org:IconInc/wordpress-bedrock-lando-starter.git
```

### Remove .git 
```
git remote remove origin
```

### Copy .lando.yml.example to .lando.yml and edit  with the name of your project
```
name: PROJECT_NAME
```

### Copy .env.example to .env with the URL of your project
```
WP_HOME=https://PROJECT_NAME.lndo.site
```

#### IMPORTANT
If you want to use a URL other than ``*.lndo.site`` who will have to add ``127.0.0.1`` to your ``/etc/hosts`` file

### Start Lando
```
lando start
```

Almost there&hellip; 

Update dependencies inside your container with:
```
lando composer update
```

## Get DB and site info
```
lando start
```
