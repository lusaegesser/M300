# Einleitung
Die LB02 Projektarbeit von Kimo Strupler und Lukas Sägesser wird hier in den folgenden Zeilen dokumentiert. 


# Projekt-Idee

Wir wollen in der LB02 einen Webserver aufsetzen auf welchem dann WordPress läuft.
Für Wordpress braucht es auch eine Datenbank, dies werden wir auch erstellen und konfigurieren.
Es wird ähnlich sein wie das Video:
https://www.youtube.com/watch?v=kIqWxjDj4IU&t=301s

Jedoch ist das video zu komploziert und man muss Wordpress herunterladen. Dies haben wir anderst gelöst. 
Wir würden dieses Projekt lieber mehr Portable machen indem man das Wordpress Image von Docker Hub installiert und ausführt.

## Services:
Wordpress:
https://hub.docker.com/_/wordpress

MYSQL:
https://www.mysql.com/de/
oder
MiriamDB:
https://hub.docker.com/_/mariadb
https://mariadb.org/


# Inhaltsverszeichnis
1. Service-Aufbau
2. Umsetzung
3. Testing
4. Quellen

## Service-Aufbau 
```
services:
  db:
    # We use a mariadb image which supports both amd64 & arm64 architecture
    image: mariadb:10.6.4-focal
    ...
  wordpress:
    image: wordpress:latest
    ports:
      - 80:80
    restart: always
    ...
```
## Umsetzung

```
$ docker compose up -d
Creating network "wordpress-mysql_default" with the default driver
Creating volume "wordpress-mysql_db_data" with default driver
...
Creating wordpress-mysql_db_1        ... done
Creating wordpress-mysql_wordpress_1 ... done
```

## Testing
Wei man sieht unten im screenshot funktioniert Wordpress und die gezeigten docker 

## Erwartetes Ergebnis

Check containers are running and the port mapping:
```
$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                 NAMES
5fbb4181a069        wordpress:latest    "docker-entrypoint.s…"   35 seconds ago      Up 34 seconds       0.0.0.0:80->80/tcp    wordpress-mysql_wordpress_1
e0884a8d444d        mysql:8.0.19        "docker-entrypoint.s…"   35 seconds ago      Up 34 seconds       3306/tcp, 33060/tcp   wordpress-mysql_db_1
```

Navigate to `http://localhost:80` in your web browser to access WordPress.

![page](output.jpg)

Stop and remove the containers

```
$ docker compose down
```

To remove all WordPress data, delete the named volumes by passing the `-v` parameter:
```
$ docker compose down -v
```

## Quellen
https://www.youtube.com/watch?v=kIqWxjDj4IU&t=301s
https://www.mysql.com/de/
https://www.php.net/manual/de/intro-whatis.php
https://hub.docker.com/_/wordpress