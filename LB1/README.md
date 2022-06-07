# Einleitung


# Inhaltsverszeichnis
1. Vagrant
2. Vagrant Webserver
3. Vagrant Persistent
4. Docker
5. Docker Image
6. Docker Run
7. Docker Persistent
8. Docker Build
9. Docker Network

## Vagrant
TextVagrant ist eine freie Ruby-Anwendung zum Erstellen und Verwalten virtueller Maschinen.

### Webserver 
Port forwarding

### persistent
VagrantFile
Synchronisation

## Docker
Docker ist eine Freie Software zur Isolierung von Anwendungen mit Hilfe von Containervirtualisierung. Docker vereinfacht die Bereitstellung von Anwendungen, weil sich Container, die alle nötigen Pakete enthalten, leicht als Dateien transportieren und installieren lassen.
https://tbzedu.sharepoint.com/sites/campus/students/it/Forms/AllItems.aspx?id=/sites/campus/students/it/_read-only/M300/2-%20Unterlagen/Docker_cheat-sheet-v2.pdf&parent=/sites/campus/students/it/_read-only/M300/2-%20Unterlagen&p=true&ga=1

### Docker Image
Images sind gebuildete Umgebungen welche als Container gestartet werden können
Images sind nicht veränderbar, sondern können nur neu gebuildet werden.
Images bestehen aus Namen und Version (TAG), z.B. ubuntu:16.04.
Wird keine Version angegeben wird automatisch :latest angefügt.

https://web.microsoftstream.com/video/df4e25df-b998-4c19-9263-17d3f32a6015?list=user&userId=91407230-9462-4d68-a2e7-13e41cfe3aaf

### Docker run
docker run ist:
- der Befehl zum Starten neuer Container
- Der bei weitem komplexesten Befehl, er unterstützt eine lange Liste möglicher Argumente
- Ermöglicht es dem Anwender, zu konfigurieren, wie das Image laufen soll, Dockerfile-Einstellungen zu überschreiben, Verbindungen zu konfigurieren und Berechtigungen und Ressourcen für den Container zu setzen.

Container sind die ausgeführten Images
Ein Image kann beliebig oft als Container ausgeführt werden
Container bzw. deren Inhalte können verändert werden, dazu werden sogenannte Union File Systems verwendet, welche nur die Änderungen zum original Image speichern.

https://web.microsoftstream.com/video/83fcd7b5-c36b-4ca8-8433-73d7aff4fb19?list=user&userId=91407230-9462-4d68-a2e7-13e41cfe3aaf


### persistent


### Docker Build
The docker build command builds Docker images from a Dockerfile and a “context”. A build's context is the set of files located in the specified PATH or URL . The build process can refer to any of the files in the context.

https://web.microsoftstream.com/video/b05df9cf-f3c9-4f52-8df4-deafbefbc2b7?list=user&userId=91407230-9462-4d68-a2e7-13e41cfe3aaf

### Docker Network
Docker networking is primarily used to establish communication between Docker containers and the outside world via the host machine where the Docker daemon is running. Docker supports different types of networks, each fit for certain use cases.

https://web.microsoftstream.com/video/96056452-99dd-49ee-9233-09fdf13583cf?list=user&userId=91407230-9462-4d68-a2e7-13e41cfe3aaf

## Quellen
Text