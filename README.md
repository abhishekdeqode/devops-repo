# Dockerizing an Flask API using Docker Compose.

## Overview
This project was created to demonstrate the implementation of flask API using Docker compose.
The API uses a database (books.db) to interact with. User can filter the retrieved data in various ways using the particular URIs.
The response to the user query is displayed in the JSON format.

## Usage
The API is dockerized which can be easily accessed from the localhost (local machine) as here, i have used the concept of port forwarding.
The default port of a flask API is 5000. And, this port of the docker container is binded to the same port of my local machine.
Now whenever we access the port 5000 on my localhost using a HTTP request, it redirects me to the container through the binded port and show me the results from the container.

## URIs
To retrieve all the data from database
```
/api/v1/resources/books/all
```
To filter the output based on keys (id, published year or author), just append the key to the previous URI

For example
```
/api/v1/resources/books?id=20

/api/v1/resources/books?published=1995

/api/v1/resources/books?author=xyz
```
