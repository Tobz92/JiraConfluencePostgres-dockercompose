# Docker compose with Jira and Confluence:

This project is aimed to setup a working environment with Jira, Confluence and Postgres in seconds.

## Requirements
- Docker and Docker Compose

## How to start

* Clone or Download this Project.
* Rename the .envexample to .env and fill in your credentials which will be used to create the database.
* If you like, rename the database names in the docker-compose.yml behind the POSTGRES_MULTIPLE_DATABASES attribute.
* If you are using Docker for Windows, make sure your drive is shared.
* In your project folder execute following statements:
```
docker-compose up
```
* Confluence running on localhost:8090 and Jira running on localhost:8080 and setup steps can be peformed on first start

## Connect to postgres database from your machine

To connect on the postgres database from your machine, use the following parameters:
- Username: defined in .env
- Password: defined in .env
- Hostname: localhost
- Database: defined in docker-compose.yml
- Port: 40699

# Jump on containers

If you want to jump on the Jira and Confluence Container from your machine:
### Confluence container
```
docker-exec -ti confluence_container /bin/bash
```
### Jira container
```
docker-exec -ti jira_container /bin/bash
```

# Todos
- [x] Add setup steps
- [ ] Mounting currently not working on Windows machine
- [ ] Document to use Jira Users in Confluence
