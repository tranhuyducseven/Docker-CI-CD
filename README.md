# This is my Docker note
*** Using for learning *** 

## Persist the Database 

## Docker compose 
### Create the compose file
- At the root of the app project, create a file named docker-compose.yml.

### Define app service in the docker-compose.yml
```yml
version: "3.7"

services:
app:
    image: node:12-alpine
    command: sh -c "yarn install && yarn run dev"
    ports:
    - 3000:3000
    working_dir: /app
    volumes:
    - ./:/app
    environment:
    MYSQL_HOST: mysql
    MYSQL_USER: root
    MYSQL_PASSWORD: secret
    MYSQL_DB: todos
```

### Define the MySQL service
```yml
version: "3.7"

 services:
   app:
     # The app service definition
   mysql:
     image: mysql:5.7
     volumes:
       - todo-mysql-data:/var/lib/mysql
     environment:
       MYSQL_ROOT_PASSWORD: secret
       MYSQL_DATABASE: todos

 volumes:
   todo-mysql-data:
```

### Run the application stack
` docker-compose up -d` 


