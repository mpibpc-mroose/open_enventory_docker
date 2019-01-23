Dockerized OpenEnventory
========================

OpenEnventory is a web application used as chemical Lan Notebook and inventory. It's
written in PHP and uses MySQL as backend. As the database users are mapped to the MySQL users
it is not possible to have multiple databases using the same user names.

To circumvent this problem the app watch "dockerized". So you can span up as many OpenEnventory instances
as you need each using it's own database.

A password sync is not possible yet (see ToDo).

Deployment
----------
See `docker-compose-multi-db.yml` for an example spanning up two instances. 

Keep in mind to extend this docker-compose.yml by an Nginx or use a local installed Nginx 
as reverse proxy.

Development
-----------
To make development a bit easier there is a `docker-compose-development.yml` spanning up a
single instance configured with XDebug running and mapping the local source to the 
container.

To Do
-----
- Python web application to set password for all instances in one place 
