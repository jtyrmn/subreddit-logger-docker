# Subreddit Logger Docker Containers

This repository contains Dockerfiles to generate all `subreddit-logger` services as well as a `docker-compose.yml` file to easily manage a `subreddit-logger` server. Note that I did this to better my understanding of Docker and that the original `subreddit-logger` project was not designed with the expectation it would be Dockerized, so this is most-likely a poor attempt.

## Involved Applications
- https://github.com/jtyrmn/subreddit-logger
- https://github.com/jtyrmn/subreddit-logger-database
- https://github.com/jtyrmn/subreddit-logger-portal
- MongoDB. *There is no Mongo container. This program connects to an external MongoDB cloud service. If you want to, it shouldn't be difficult to add the Mongo container and edit the `MONGODB_CONNECTION_STRING` and `MONGODB_DATABASE_NAME` environment variables.*

## Setup
All configuration files are to be put in the `./shared/` directory. See the example files or the various repositories of all the services for details on configuration. You also need a MongoDB instance somewhere, see above. You can then run the services using `docker compose up`.