# massr-on-docker-compose

## overview

running Massr on docker-compose with these containers; `mongo` and `memcached` .
via. https://github.com/tdtds/massr

## require

- Docker environment (with Docker Compose)

## usage

set your Twitter API-key to `.env` .

```
TWITTER_CONSUMER_ID=YOUR_TWITTER_API_KEY
TWITTER_CONSUMER_SECRET=YOUR_TWITTER_API_SECRET
```

make directory for mongodb datastore.

```
$ mkdir -p data/db
```

run

```
$ docker-compose up -d --build
```

Enjoy!
