# Important commands for intereacting with redis

## redis-cli

redis-cli is a command line interface for interacting with redis. Unserstanding redis-cli is useful for understanding the redis implementation in Python.

## Basic commands and getting started

To start, connect to your redis instance. If you run your container on the non-default port (defualt: 6379), you will need to specify the port with the `-p` flag. Here is the basic command to connect to a redis instance running on port 6379:

`redis-cli`

To see if there are any keys in the database:

`KEYS *`

To check the type of a key:

`TYPE <key>`

To delete all of the data:

`FLUSHDB`

### ReJSON-RL (JSON) data type

As the name suggests, ReJSON stores JSON structures! 

You can add JSON data to Redis with:

`JSON.SET <key> $ 'json'`

Given a key of type ReJSON-RL, you can retrieve data with:

`JSON.GET <key>`


### zset (sorted set) data type

How to query a sorted set in redis?

`ZRANGE <key> 0 -1 WITHSCORES`

### Geographic infromation in sorted sets

You can add geographic data with:

`GEOADD <key> <lng> <lat> <member>`

Given a specific member id, you can retrieve the lat lng data with:

`GEOPOS <key> <member>`

You can query geographic regions and return all members that are within:

`GEOSEARCH <key> FROMLONLAT <lng> <lat> BYBOX <width> <height> KM ASC WITHCOORD`


