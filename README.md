# Prerequisites

Make sure you have already installed both Docker Engine and 
Docker Compose.

I have created a file docker-compose.yml with the following service so we can connect PostgreSql via docker:

```
services:
  pgdb:
    image: postgres
    environment:
      POSTGRES_USER: root
      POSTGRES_PASSWORD: pass
      POSTGRES_DB: bookdb         
    ports:
      - 5432:5432
```

# Build and run your app with Compose

* `git clone https://github.com/mdoklea/docker-with-postgresql.git`
* From your project directory, start up your application by running `docker-compose up` 
* Enter `http://localhost:8090 ` in a browser to see the application running
* Voilà the admin page:

  ![DB Admin Page](/images/db-admin.png)
  
  
* You can bring everything down, removing the containers entirely, with the down command.
`docker-compose down`
