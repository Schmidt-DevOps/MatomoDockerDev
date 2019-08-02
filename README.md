# Purpose

Set up a development environment for Matomo quick & easy.

# Usage

```
docker-compose up
```

Then open http://localhost:3000 in your web browser. Enter the following DB setup:

1. Server: mariadb
1. User: root
1. Password: pass
1. Database: matomo

Follow the instructions.

# Reset the environment

Note that this wipes the database irrevocably:

``` 
docker exec -it matomodockerdev_matomo_1 rm /var/www/html/config/config.ini.php
docker exec -it matomo-mariadb mysql -uroot -ppass -e "DROP DATABASE matomo;"
```

Then open http://localhost:3000/ in your webbrowser.

# piwik-docker-dev
Development docker-compose.yml for Piwik.

Original by https://github.com/Alexcn/piwik-docker-dev

