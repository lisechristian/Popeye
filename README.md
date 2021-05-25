# Popeye

The goal of this project is to containerize and define the deployment of a simple web poll application

There are five elements constituting the application:

  1. Poll, a flask Python web application that gathers votes and push them into a Redis queue.

  2.  Redis, which holds the votes sent by the Poll application, awaiting for them to be consumed by the Worker.

  3. Worker, a java application which consumes the votes being in the Redis queue, and stores them into a PostgreSQL database

  4. PostgreSQL database, which (persistently) stores the votes stored by the Worker.

  5.  Result, a Node.js web application that fetches the votes from the database and displays the result

![image](https://user-images.githubusercontent.com/72029442/119541534-cc911d00-bd8e-11eb-9e3c-bac9870f828c.png)


Built With

    Docker-compose
