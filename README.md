# POPEY PROJECT
Welcome to my Popeye project, my first DevOps project. The purpose of this project was to create 3 images. During this project, I learned the bases of container applications and describe multicontainers infrastructures with Docker and Docker Compose.


### PARTS OF THE PROJECT
- **Poll**: a Flask Python web application that gathers votes and push them into a Redis queue
- **Redis queue**: which holds the votes sent by the Poll application, awaiting for them to be consumed by
the Worker
- **Worker**: a Java application which consumes the votes being in the Redis queue, and stores them into
a PostgreSQL database
- **PostreSQL database**: which (persistently) stores the votes stored by the Worker
- **Result**: a Node.js web application that fetches the votes from the database and displays the result

![](/assets/schema.png "Schema")
